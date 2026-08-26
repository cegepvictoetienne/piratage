# Reconnaissance passive

Deux types de reconnaissance :

- Reconnaissance active
- Reconnaissance passive

## Reconnaissance passive

La reconnaissance passive est toute activité qui n'envoie pas d'information à la cible.

## Ingénierie sociale

La reconnaissance passive est essentielle pour une attaque d'ingénierie sociale. L'ingénierie sociale est une forme de piratage où le pirate cherche à convaincre un être humain de faire une action lui permettant de prendre contrôle d'un système ou collecter des informations confidentielles.  

## Outils d'intelligence du domaine public

Appellés **OSINT** (Open Source Intelligence), les outils d'intelligence du domaine public regorge d'information qui permettent à un pirate de bien connaître sa cible. Lors de la reconnaissance passive, il est essentiel de bien connaître les systèmes informatiques de la cible, mais aussi d'en connaître les personnes qui forment l'entreprise.  

!!! important  
    Il est beaucoup plus facile de pirater une entreprise à travers ses employés que via leurs systèmes.  

Quelques outils pour découvrir de l'information sur une entreprise et ses employés :  

Outil  | Utilité    
--|--
[LinkedIn](https://www.linkedin.com) | On peut voir facilement la liste des employés d'une entreprise    
[Registre des entreprise (Québec)](https://www.quebec.ca/entreprises-et-travailleurs-autonomes/obtenir-renseignements-entreprise/recherche-registre-entreprises/acceder-registre-entreprises)  |  Donne de l'information sur l'entreprise, incluant le nom du propriétaire et possiblement des adresses 
[CanLII](https://www.canlii.org/fr/)  |  Tous les documents des tribunaux canadiens  
[Ancestry](https://www.ancestry.ca)  |  Pour trouver des informations sur les membres de la famille, mariages, divorces, etc.

[OSINT Québec - Regroupement d'outils de données ouvertes au Québec](https://osintquebec.profinfo.ca)  

## Medias sociaux  

[Social Searcher](https://www.social-searcher.com)  

## Bug Me Not  

Pas un site de recherche en soi, mais permet de trouver des codes utilisateurs pour certains sites qui oblige des logins pour utiliser leurs services. 

[Bug Me Not](https://bugmenot.com/)  

## Outil de recherche 

Voici un outil de recherche pour diverses communautés : 

[Intel Techniques](https://inteltechniques.com/tools/Communities.html)  

## Mots de passe et sites utilisés par un utilisateur  

[DeHashed](https://dehashed.com/)  
[Have I Been Pwned](https://haveibeenpwned.com/)  
[LeakPeak - mots de passe partiels](https://leakpeek.com/)  
[BreachDirectory](https://breachdirectory.org/)  Essayez avec test@email.com  
[Outil pour décrypter MD5 et SHA1](https://md5decrypt.net/en/Sha1/)  

## Outils pour vérifier si un courriel existe et est valide  

[Hunter Verify](https://hunter.io/verify/etienne@kerzo.ca)  

## Si vous trouvez un code utilisateur, vérifiez quel média social utilise ce code  

[Username Search](https://instantusername.com)  

## Outil pour vérifier si un server coule des fichiers qu'il ne devrait pas  

[Leakix](https://leakix.net/)  

## Outil de recherche général  

[IntelligenceX](https://intelx.io/)  

## Métadonnées dans les images  

Les images ont des métadonnées que l'on nomme EXIF.  

L'outil [ExifTool](https://exiftool.org) permet de lire les données, incluant les données GPS.  

``` console
exiftool -p '$GPSLatitude#, $GPSLongitude#' image.jpg 
``` 

Donne les coordonnées GPS en décimales de l'appareil qui a pris la photo.  

Exemple :  

![Voyage](../images/img8221.jpg)  

```
ExifTool Version Number         : 13.55
File Name                       : img8221.jpg
Directory                       : .
File Size                       : 2000 kB
File Modification Date/Time     : 2026:08:07 09:41:52-04:00
File Access Date/Time           : 2026:08:07 09:45:38-04:00
File Inode Change Date/Time     : 2026:08:07 09:45:36-04:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
Exif Byte Order                 : Big-endian (Motorola, MM)
Make                            : Apple
Camera Model Name               : iPhone 5
Orientation                     : Horizontal (normal)
X Resolution                    : 72
Y Resolution                    : 72
Resolution Unit                 : inches
Software                        : 7.0.2
Modify Date                     : 2013:10:26 12:36:16
Y Cb Cr Positioning             : Centered
Exposure Time                   : 1/20
F Number                        : 2.4
Exposure Program                : Program AE
ISO                             : 200
Exif Version                    : 0221
Date/Time Original              : 2013:10:26 12:36:16
Create Date                     : 2013:10:26 12:36:16
Components Configuration        : Y, Cb, Cr, -
Shutter Speed Value             : 1/20
Aperture Value                  : 2.4
Brightness Value                : 1.180513595
Metering Mode                   : Multi-segment
Flash                           : Off, Did not fire
Focal Length                    : 4.1 mm
Subject Area                    : 1630 1221 734 440
Maker Note Version              : 0
Run Time Scale                  : 1000000000
Run Time Epoch                  : 0
Run Time Value                  : 313078813370500
Run Time Flags                  : Valid
AE Stable                       : Yes
AE Target                       : 156
AE Average                      : 143
AF Stable                       : Yes
Sub Sec Time Original           : 542
Sub Sec Time Digitized          : 542
Flashpix Version                : 0100
Color Space                     : sRGB
Exif Image Width                : 3264
Exif Image Height               : 2448
Sensing Method                  : One-chip color area
Scene Type                      : Directly photographed
Exposure Mode                   : Auto
White Balance                   : Auto
Focal Length In 35mm Format     : 33 mm
Scene Capture Type              : Standard
Lens Info                       : 4.12mm f/2.4
Lens Make                       : Apple
Lens Model                      : iPhone 5 back camera 4.12mm f/2.4
GPS Latitude Ref                : North
GPS Longitude Ref               : West
GPS Altitude Ref                : Above Sea Level
GPS Time Stamp                  : 16:36:12.41
GPS Img Direction Ref           : True North
GPS Img Direction               : 331.3275109
Compression                     : JPEG (old-style)
Thumbnail Offset                : 1254
Thumbnail Length                : 8994
Image Width                     : 3264
Image Height                    : 2448
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Run Time Since Power Up         : 3 days 14:57:59
Aperture                        : 2.4
Image Size                      : 3264x2448
Megapixels                      : 8.0
Scale Factor To 35 mm Equivalent: 8.0
Shutter Speed                   : 1/20
Create Date                     : 2013:10:26 12:36:16.542
Date/Time Original              : 2013:10:26 12:36:16.542
Thumbnail Image                 : (Binary data 8994 bytes, use -b option to extract)
GPS Altitude                    : 64 m Above Sea Level
GPS Latitude                    : 45 deg 25' 46.48" N
GPS Longitude                   : 75 deg 42' 30.23" W
Circle Of Confusion             : 0.004 mm
Field Of View                   : 57.2 deg
Focal Length 35mm Equiv         : 4.1 mm (35 mm equivalent: 33.0 mm)
GPS Position                    : 45 deg 25' 46.48" N, 75 deg 42' 30.23" W
Hyperfocal Distance             : 1.89 m
Light Value                     : 5.8
Lens ID                         : iPhone 5 back camera 4.12mm f/2.4
``` 

Si on convertit la position GPS en décimales :  

```
45.4295777777778, -75.7083972222222
```

[Dans Google Maps](https://www.google.com/maps/place/45°25'46.5%22N+75°42'30.2%22W/@45.4295815,-75.7109721,17z/data=!3m1!4b1!4m4!3m3!8m2!3d45.4295778!4d-75.7083972?entry=ttu&g_ep=EgoyMDI2MDgwNC4wIKXMDSoASAFQAw%3D%3D)  


## Ordinateurs infectés?  

Outil de recherche pour voir si une entreprise a eu une cyber attaque :  

[HudsonRock](https://www.hudsonrock.com/threat-intelligence-cybercrime-tools)  

## Recherche de sous-domaines

Souvent, les sous-domaines sont des serveurs dans la DMZ de l’entreprise, bons points d’entrées dans le réseau.

Outils utilisés :

[DNS Dumpster](https://dnsdumpster.com/)

[NMMapper's Subdomain Finder](https://www.nmmapper.com/sys/tools/subdomainfinder/)


## Testez vos connaissances  

[Petit quiz sur la reconnaissance passive](https://forms.office.com/r/7qNdDYPMpc)  
