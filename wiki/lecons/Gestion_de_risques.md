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

!!! important  
    Prenez quelques minutes pour faire votre [cartographie](../outils/cartographie.md) de la leçon d'aujourd'hui!   

## Testez vos connaissances  

[Petit quiz sur la gestion de risques](https://forms.office.com/r/pANFZCZ8h4)  
