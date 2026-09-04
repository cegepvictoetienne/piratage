# Gestion de risques

## Définitions des termes les plus importants

**Actif** (_asset_) : N'importe quoi dans un environnement qui doit être protégé. N'importe quoi qui peut être utilisé dans une tâche ou un processus d'affaires. Ce peut être un fichier, un service réseau, un programme, un produit, une infrastructure TI, une base de données, du matériel informatique, un système d'exploitation, etc. Si l'entreprise y voit une valeur assez importante pour la protéger, c'est un actif.

**Valeur d'un actif** (_asset valuation_) : Valeur monétaire assignée à un actif. Cela inclus le coût direct d'achat et les coûts associés non-monétaires. Les autres coûts peuvent être le développement, le maintien et le support.

**Menace** (_threat_) : Une menace est une occurence qui peut causer dénouement non désirable pour une organisation. Une menace peut être toute action ou inaction qui peut causer du dommage, de la destruction, une modification, une perte, une fuite d'information ou qui peut empêcher l'utilisation d'un actif. Ce peut être accidentel ou intentionnel. Une menace peut venir d'une personne, une organisation, du matériel, de réseaux ou même de la nature. Ce peut être un pirate, un employé, un tremblement de terre ou un feu, par exemple.

**Vulnérabilité** (_vulnerability_) : Une vulnérabilité est une faille ou une faiblesse dans un actif ou l'absence de précautions ou de contremesures.

**Exposition** (_exposure_) : L'exposition est être susceptible à une perte d'un actif dû à d'une menace. Il y a une possibilité que l'actif soit vulnérable ou qu'il puisse être exploité par une personne menaçante.

**Risque** (_risk_) : Le risque est la possibilité qu'une menace exploite une vulnérabilité pour causer du tort à un actif. C'est une évaluation de probabilité d'occurence, de possibilité ou de chance. Plus il y a de chance qu'un menace se concrétise, plus le risque est grand. La formule suivante représente bien le risque :

`risque = menace * vulnérabilité`

Dans ce sens, réduire la menace ou la vulnérabilité réduit le risque.

**Mesure de protection** (_safeguard_) : Une mesure de protection est n'importe quoi qui enlève ou réduit une vulnérabilité ou protège d'une menace. Ce peut être l'installation de rustine (_patch_), la configuration de systèmes, l'embauche de gardes de sécurité, installer un pare-feu, etc. Ce n'est pas nécessaire de faire l'achat d'équipement ou de logiciel pour être considéré une mesure, parfois une simple reconfiguration on un retrait d'actif est suffisant.

**Attaque** (_attack_) : Une attaque est l'exploitation d'une vulnérabilité par une personne menaçante. C'est une utilisation délibérée d'une vulnérabilité pour causer des dommages à l'entreprise.

**Intrusion** (_breach_) : Une intrusion est une personne menaçante qui contourne un mécanisme de sécurité. Quand une intrusion est combinée à une attaque, on appelle ça une pénétration.

## Identifier les menaces et vulnérabilités

Il faut considérer les éléments suivants lors de l'identification de menaces et vulnérabilités :

- Les virus
- Activités criminelles par des utilisateurs autorisés
- Mouvement (vibration, secousses, etc.)
- Attaques intentionnelles
- Réorganisations
- Épidémies et pandémies
- Pirates malicieux
- Employés frustrés
- Erreurs par les utilisateurs
- Désastres naturels (tremblement de terre, inondations, feux, volcans, tornades, etc.)
- Dommages physiques (écraser, coupure de câbles, etc.)
- Mauvaise utilisation de données, ressources ou services
- Erreurs de processus, dépassement de pile
- Abus de privilèges par les employés
- Températures extrêmes
- Fluctuation énergétiques
- Perte de données
- Erreurs de programmation
- Intrus
- Faille d'équipement
- Vol physique
- Ingénierie sociale

## Évaluation des risques

Première chose : **il est impossible d'éliminer à 100% les risques**

Seconde chose : L'entreprise peut choisir d'accepter le risque au lieu de le réduire.

### Analyse de risques quantitative

L'analyse de risques quantitative est la méthode qui offre des pourcentages de probabilités concrets. Ça veut dire que nous pouvons assigner une valeur monétaire au risque, à la perte potentielle et aux coûts de protection. Cependant, ce n'est pas tous les risques qui peuvent être évalués de manière quantitative.

Voici les 6 étapes de l'analyse de risques quantitative :  
1. Déterminer la valeur de l'actif : **AV** (_Asset Value_)  
2. Produire une liste de menaces pour chaque actif, calculer le facteur d'exposition **EF** (_Exposure Factor_) et la perte prévue unique **SLE** (_Single Loss Expectancy_)  
3. Faire l'analyse des menaces pour calculer la probabilité de se produire dans une année, ce qu'on appelle la fréquence annualisée d'occurence **ARO** (_Annualised Rate of Occurence_)  
4. Calculer le potentiel de perte par menace en calculant la perte prévue annualisée **ALE** (_Annualised Loss Expectency_)  
5. Rechercher les mesures de protection et calculer les ARO et ALE basé sur ces mesures.  
6. Faire une analyse de coûts et bénéfices pour chaque mesure. Sélectionner la mesure la plus appropriée  

Ex: Vous avez acheté une voiture pour 1 500$. Votre assureur vous donne le choix d'une assurance de base à 500$ par année ou une assurance "valeur à neuf" pour 1 000$ par année, avec un déductible de 300$. En 5 ans de conduite, vous n'avez fait qu'un accident mineur avec des dommages de moins de 500$. Un accident pourrait diminuer de 40% la valeur de votre voiture.

Variable  | Formule | Valeur  
--|--|--  
AV  | $ | 1 500$  
EF  | % | 40%
SLE | SLE = AV * EF |  1 500$ * 40% = 600$  
ARO | # / année | 1 / 5 = 20% (1 fois au 5 ans)
ALE | ALE = SLE * ARO | 600$ * 20% = 120$  

Donc, votre risque d'accident vaut 120$ par année. Croyez-vous que payer un surplus de 500$ par année à votre assurance vaut la peine?

<div class="qra-calc">
  <div class="qra-calc__header">
    <span class="qra-calc__icon">🧮</span>
    <div>
      <p class="qra-calc__title">Calculateur d'analyse de risques quantitative</p>
      <p class="qra-calc__subtitle">Entrez vos valeurs pour calculer le SLE et l'ALE, puis évaluez si une mesure de protection est financièrement justifiée.</p>
    </div>
  </div>

  <div class="qra-calc__grid">
    <div class="qra-calc__col">
      <h4>1. Actif et menace</h4>
      <label>Valeur de l'actif — AV ($)
        <input type="number" id="qra-av" value="1500" min="0" step="any">
      </label>
      <label>Facteur d'exposition — EF (%)
        <input type="number" id="qra-ef" value="40" min="0" max="100" step="any">
      </label>
      <label>Fréquence annualisée — ARO (occurrences / an)
        <input type="number" id="qra-aro" value="0.2" min="0" step="any">
      </label>
      <p class="qra-calc__hint">Ex. : 0,2 = une fois tous les 5 ans. 3 = trois fois par année.</p>

      <h4>2. Mesure de protection <span class="qra-calc__optional">(optionnel)</span></h4>
      <label>Coût annuel de la mesure — ACS ($)
        <input type="number" id="qra-acs" value="" min="0" step="any" placeholder="ex. : 500">
      </label>
      <label>EF après la mesure (%)
        <input type="number" id="qra-ef2" value="" min="0" max="100" step="any" placeholder="ex. : 10">
      </label>
      <label>ARO après la mesure (occurrences / an)
        <input type="number" id="qra-aro2" value="" min="0" step="any" placeholder="ex. : 0,2">
      </label>

      <div class="qra-calc__actions">
        <button type="button" id="qra-example">Charger l'exemple du cours</button>
        <button type="button" id="qra-reset" class="qra-calc__btn-ghost">Réinitialiser</button>
      </div>
    </div>

    <div class="qra-calc__col qra-calc__results">
      <h4>Résultats</h4>
      <div class="qra-calc__result-row">
        <span>SLE — perte prévue unique</span>
        <strong id="qra-sle">—</strong>
      </div>
      <div class="qra-calc__result-row qra-calc__result-row--total">
        <span>ALE — perte prévue annualisée</span>
        <strong id="qra-ale">—</strong>
      </div>

      <div id="qra-safeguard-block" hidden>
        <h4>Avec la mesure de protection</h4>
        <div class="qra-calc__result-row">
          <span>ALE après la mesure</span>
          <strong id="qra-ale2">—</strong>
        </div>
        <div class="qra-calc__result-row">
          <span>Réduction annuelle du risque</span>
          <strong id="qra-reduction">—</strong>
        </div>
        <div class="qra-calc__result-row qra-calc__result-row--total">
          <span>Valeur nette de la mesure</span>
          <strong id="qra-value">—</strong>
        </div>
        <p id="qra-verdict" class="qra-calc__verdict"></p>
      </div>
    </div>
  </div>
</div>

<style>
.qra-calc {
  border: 1px solid var(--ls-surface-high);
  border-radius: 0.75rem;
  background: var(--ls-surface-low);
  padding: 1.5rem;
  margin: 1.5rem 0 2rem;
}

.qra-calc__header {
  display: flex;
  gap: 0.75rem;
  align-items: flex-start;
  margin-bottom: 1.25rem;
}

.qra-calc__icon { font-size: 1.75rem; line-height: 1; }

.qra-calc__title {
  margin: 0;
  font-family: "Space Grotesk", "Inter", sans-serif;
  font-weight: 600;
  font-size: 1.05rem;
  color: var(--ls-text-headline);
}

.qra-calc__subtitle {
  margin: 0.25rem 0 0;
  font-size: 0.85rem;
  color: var(--ls-text-caption);
}

.qra-calc__grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.5rem;
  align-items: start;
}

@media (max-width: 640px) {
  .qra-calc__grid { grid-template-columns: 1fr; }
}

.qra-calc__col h4 {
  margin: 0 0 0.75rem;
  font-size: 0.75rem;
  text-transform: uppercase;
  letter-spacing: 0.04em;
  color: var(--ls-text-caption);
  font-weight: 700;
}

.qra-calc__col h4:not(:first-child) { margin-top: 1.5rem; }

.qra-calc__optional { text-transform: none; font-weight: 400; letter-spacing: normal; }

.qra-calc__hint {
  margin: -0.4rem 0 0.75rem;
  font-size: 0.75rem;
  color: var(--ls-text-caption);
}

.qra-calc label {
  display: block;
  font-size: 0.85rem;
  color: var(--ls-text-body);
  margin-bottom: 0.75rem;
}

.qra-calc input[type="number"] {
  display: block;
  width: 100%;
  margin-top: 0.3rem;
  box-sizing: border-box;
  padding: 0.5rem 0.65rem;
  border-radius: 0.4rem;
  border: 1px solid var(--ls-surface-high);
  background: var(--ls-surface-main);
  color: var(--ls-text-headline);
  font-size: 0.95rem;
  font-family: inherit;
}

.qra-calc input[type="number"]:focus {
  outline: none;
  border-color: var(--ls-primary);
  box-shadow: 0 0 0 3px rgba(13, 148, 136, 0.15);
}

.qra-calc__actions {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.qra-calc__actions button {
  border: none;
  border-radius: 9999px;
  padding: 0.5rem 1rem;
  font-size: 0.8rem;
  font-weight: 600;
  cursor: pointer;
  font-family: inherit;
  transition: opacity 0.15s ease, transform 0.15s ease;
  background: var(--ls-primary);
  color: #fff;
}

.qra-calc__actions button.qra-calc__btn-ghost {
  background: transparent;
  color: var(--ls-text-caption);
  border: 1px solid var(--ls-surface-high);
}

.qra-calc__actions button:hover { opacity: 0.85; }
.qra-calc__actions button:active { transform: scale(0.97); }

.qra-calc__results {
  background: var(--ls-surface-main);
  border: 1px solid var(--ls-surface-high);
  border-radius: 0.5rem;
  padding: 1rem 1.1rem;
}

.qra-calc__result-row {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  gap: 1rem;
  padding: 0.5rem 0;
  border-bottom: 1px dashed var(--ls-surface-high);
  font-size: 0.88rem;
  color: var(--ls-text-body);
}

.qra-calc__result-row strong {
  color: var(--ls-text-headline);
  font-family: "Space Grotesk", "Inter", sans-serif;
  white-space: nowrap;
}

.qra-calc__result-row--total {
  border-bottom: none;
  padding-top: 0.65rem;
  font-weight: 600;
}

.qra-calc__result-row--total strong {
  color: var(--ls-primary-dark);
  font-size: 1.05rem;
}

#qra-safeguard-block {
  margin-top: 0.5rem;
  padding-top: 0.75rem;
  border-top: 2px solid var(--ls-surface-high);
}

.qra-calc__verdict {
  margin: 0.75rem 0 0;
  padding: 0.6rem 0.75rem;
  border-radius: 0.4rem;
  font-size: 0.85rem;
  font-weight: 600;
}

.qra-calc__verdict--good { background: rgba(43, 155, 70, 0.14); color: #1c7a37; }
.qra-calc__verdict--bad { background: rgba(153, 27, 27, 0.12); color: var(--ls-alert); }
</style>

<script>
(function () {
  var $ = function (id) { return document.getElementById(id); };
  var fmt = function (n) {
    if (!isFinite(n)) return '—';
    return n.toLocaleString('fr-CA', { style: 'currency', currency: 'CAD', maximumFractionDigits: 2 });
  };
  var num = function (el) {
    var v = parseFloat(el.value);
    return isFinite(v) ? v : NaN;
  };

  var av = $('qra-av'), ef = $('qra-ef'), aro = $('qra-aro');
  var acs = $('qra-acs'), ef2 = $('qra-ef2'), aro2 = $('qra-aro2');
  var sleOut = $('qra-sle'), aleOut = $('qra-ale');
  var ale2Out = $('qra-ale2'), reductionOut = $('qra-reduction'), valueOut = $('qra-value');
  var verdict = $('qra-verdict'), safeguardBlock = $('qra-safeguard-block');

  function calculer() {
    var AV = num(av), EF = num(ef), ARO = num(aro);
    var SLE = AV * (EF / 100);
    var ALE = SLE * ARO;
    sleOut.textContent = fmt(SLE);
    aleOut.textContent = fmt(ALE);

    var hasSafeguard = acs.value !== '' || ef2.value !== '' || aro2.value !== '';

    if (hasSafeguard) {
      safeguardBlock.hidden = false;

      var effEF2 = ef2.value !== '' ? num(ef2) : EF;
      var effARO2 = aro2.value !== '' ? num(aro2) : ARO;
      var effACS = acs.value !== '' ? num(acs) : 0;

      var SLE2 = AV * (effEF2 / 100);
      var ALE2 = SLE2 * effARO2;
      var reduction = ALE - ALE2;
      var valeur = reduction - effACS;

      ale2Out.textContent = fmt(ALE2);
      reductionOut.textContent = fmt(reduction);
      valueOut.textContent = fmt(valeur);

      if (isFinite(valeur)) {
        verdict.className = 'qra-calc__verdict ' + (valeur >= 0 ? 'qra-calc__verdict--good' : 'qra-calc__verdict--bad');
        verdict.textContent = valeur >= 0
          ? '✅ La mesure est justifiée : elle réduit le risque de ' + fmt(reduction) + '/an pour un coût de ' + fmt(effACS) + '/an.'
          : '⚠️ La mesure coûte plus cher (' + fmt(effACS) + '/an) que la réduction de risque qu’elle apporte (' + fmt(reduction) + '/an).';
      } else {
        verdict.className = 'qra-calc__verdict';
        verdict.textContent = '';
      }
    } else {
      safeguardBlock.hidden = true;
    }
  }

  [av, ef, aro, acs, ef2, aro2].forEach(function (el) {
    el.addEventListener('input', calculer);
  });

  $('qra-example').addEventListener('click', function () {
    av.value = 1500;
    ef.value = 40;
    aro.value = 0.2;
    acs.value = '';
    ef2.value = '';
    aro2.value = '';
    calculer();
  });

  $('qra-reset').addEventListener('click', function () {
    av.value = '';
    ef.value = '';
    aro.value = '';
    acs.value = '';
    ef2.value = '';
    aro2.value = '';
    calculer();
  });

  calculer();
})();
</script>

## Analyse de risques qualitative

Une analyste de risques qualitative est basée sur des scénarios. C'est basé sur des échelles pour évaluer les risques, coûts et effets. Nous faisons surtout appel à votre jugement, intuition et expérience.

Par exemple, pour les risques reliés à un centre de données :

Risque  | Probabilité  | Coûts
--|---|--
Feu  | 3 - Moyen  | $$$  
Tremblement de terre  | 4 - Faible  | $$  
Éruption volcanique  | 5 - Très faible   | $$$  

Dans cet exemple, il est plus important de réduire les risques de feu.

## Réponses aux risques

L'entreprise peut répondre de plusieurs manières aux risques.

### Atténuation du risque

Atténuer ou réduire le risque est l'application de mesures de protection pour éliminer les vulnérabilités ou bloquer les menaces.

## Transfert du risque

Transférer le risque est le placement du coût de la perte chez une autre entité. Par exemple, acheter une assurance contre le feu est un transfert de risque vers la compagnie d'assurance.

## Accepter le risque

Dans certains cas, l'entreprise décide d'accepter de vivre avec le risque et les pertes potentielles au lieu d'investir dans une solution d'atténuation ou de transfert du risque.

Aussi appelé l'appétit pour le risque.

## Testez vos connaissances  

[Petit quiz sur la gestion de risques](https://forms.office.com/r/pANFZCZ8h4)  
