## Créer une fausse preuve vaccinale avec node.js  

La preuve vaccinale du Gouvernement du Québec se base sur un standard international nommé [Smart Health Card](https://smarthealth.cards).  

Voici un exemple de code qui permet de créer une preuve de vaccin. Notez que la preuve n'est pas valide et cette démonstration est pour fins éducatives.

## Prérequis  

node.js  

Les modules :  
- node-jose  
- qrcode  

## Le code  

L'information contenue dans le code QR :  

```
const fhirBundle = {
  "resourceType": "Bundle",
  "type": "collection",
  "entry": [
  {
    "resource": {
      "resourceType": "Patient",
      "name": [
        {
          "family": [
            "Légo"
          ],
          "given": [
            "François"
          ]
        }
      ],
      "birthDate": "1957-05-26",
      "gender": "Male"
    }
  },
  {
    "resource": {
      "resourceType": "Immunization",
      "vaccineCode": {
        "coding": [
          {
            "system": "http://hl7.org/fhir/sid/cvx",
            "code": "207"
          }
        ]
      },
      "patient": {
        "reference": "resource:0"
      },
      "lotNumber": "MBS",
      "status": "Completed",
      "occurrenceDateTime": "2021-05-04T04:00:00+00:00",
      "location": {
        "reference": "resource:0",
        "display": "Québec"
      },
      "protocolApplied": {
        "doseNumber": 1,
        "targetDisease": {
          "coding": [
            {
              "system": "http://browser.ihtsdotools.org/?perspective=full&conceptId1=840536004",
              "code": "840536004"
            }
          ]
        }
      },
      "note": [
        {
          "text": "MOD COVID-19"
        }
      ]
    }
  },
  {
    "resource": {
      "resourceType": "Immunization",
      "vaccineCode": {
        "coding": [
          {
            "system": "http://hl7.org/fhir/sid/cvx",
            "code": "207"
          }
        ]
      },
      "patient": {
        "reference": "resource:0"
      },
      "lotNumber": "HJS",
      "status": "Completed",
      "occurrenceDateTime": "2021-06-29T04:00:00+00:00",
      "location": {
        "reference": "resource:0",
        "display": "Québec"
      },
      "protocolApplied": {
        "doseNumber": 2,
        "targetDisease": {
          "coding": [
            {
              "system": "http://browser.ihtsdotools.org/?perspective=full&conceptId1=840536004",
              "code": "840536004"
            }
          ]
        }
      },
      "note": [
        {
          "text": "MOD COVID-19"
        }
      ]
    }
  }
]
}

const expandedHealthCard = {
  "iss": "https://smarthealth.cards/examples/issuer",
  "nbf": Date.now() / 1000,
  "vc": {
    "@context": [
      "https://www.w3.org/2018/credentials/v1"
    ],
    "type": [
      "VerifiableCredential",
      "https://smarthealth.cards#health-card",
      "https://smarthealth.cards#immunization",
      "https://smarthealth.cards#covid19"
    ],
    "credentialSubject": {
        "fhirVersion": "4.0.1",
        "fhirBundle": fhirBundle
    }
  }
}

// Enlève les espaces  
const noWhiteSpaceHealthCard = JSON.stringify(expandedHealthCard)

// Compresser les données avec DEFLATE

const compressedPayload = zlib.deflateRawSync(noWhiteSpaceHealthCard)
```

Signature des données :  

```
var jose = require('node-jose');

const kstore = jose.JWK.createKeyStore()

let signingKey;

kstore.generate("EC", "P-256").
        then(function(result) {
          // {result} is a jose.JWK.Key
          signingKey = result;
        });

const fields = { zip: 'DEF' }

let jws;

jose.JWS.createSign({ format: 'compact', fields }, signingKey)
    .update(Buffer.from(compressedPayload))
    .final()
    .then(function(result) {
        jws = result;
});

jose.JWS.createVerify(signingKey)
    .verify(jws).then(function(result) {
    console.log(result)
})


```


Conversion en code QR numérique :  

```
// Convert to numeric mode QR

// This code snippet was adapted/taken from https://github.com/smart-on-fhir/health-cards/blob/152a4f83b223b5fd14027f765e957e290649f2c0/generate-examples/src/index.ts#L173
const numericJWS = jws.split('')
    .map((c) => c.charCodeAt(0) - 45)
    .flatMap((c) => [Math.floor(c / 10), c % 10]) //Need to maintain leading zeros
    .join('')

const qrCodeData = 'shc:/' + numericJWS
```

Création du code QR :  

```
var QRCode = require('qrcode')

const segments = [
    {data: 'shc:/', mode: 'byte'},
    {data: numericJWS, mode: 'numeric'}
]

let qrSVG
QRCode.toString(segments,{type: 'svg', errorCorrectionLevel: 'low', width: 400, version: 24 }).then(function(result){
    qrSVG = result
    $$.svg(qrSVG)
})

// Also print as PNG for scanning later on.


QRCode.toFile('./qrcode.png', segments, {width: 400, version: 24})

```
