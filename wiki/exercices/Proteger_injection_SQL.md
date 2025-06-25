# Exercices - Protéger injection SQL

# Quiz sur la théorie   

[Petit quiz sur la protection d'injection SQL](https://forms.office.com/r/9NLyJBkyV3)  

# Exercice obligatoire  

## Code source  

Le code source de l'application MonMur se trouve dans la VM MonMur.

## VM contenant l'application Web  

L'application MonMur se trouve sur la VM [MonMur](../labo/Installation_MonMur_VirtualBox.md).

Durant cet exercice, vous aurez à sécuriser l'application contre les vulnérabilités suivantes :  

- Injection SQL
- Mauvaise utilisation de la base de données

Avant de modifier l'application, testez-là pour les failles d'injection SQL. Utilisez SQLMap pour vous aider.  

Modifier l'application à tous les endroits où la base de données est utilisée.

L'application se trouve dans `/var/www`.
