# Exercices - Injections SQL 

Les exercices d'injection SQL vont reproduire ce que le professeur a fait en classe.

Vous aurez besoin de Kali et de Metasploitable.

Allez sur la page de DVWA de Metasploitable via Firefox sur Kali.  

Pour se connecter, user : admin password : password  

## Reconnaissance active  

Faites les étapes de la reconnaissance active :  

Notez que vous ne pouvez pas prendre les exemples en classe de manière verbatim, le professeur a changé le type d'assignation dans DVWA.

1. Déterminer le type d'assignation des valeurs dans la requête  
2. Déterminer le nombre de colonnes que la requête retourne  
3. Trouver les informations sur la base de données
4. Faire la liste des tables
5. Faire la liste des champs des tables

## Extraction de la table users

Faites l'extraction de la table users avec une injection SQL manuelle.

## Utilisation de SQLMap

Dans Kali, faites les étapes suivantes  :

1. Utiliser BurpSuite et Firefox pour extraire les cookies
2. Utiliser SQLMap pour découvrir la BD, la liste des table et le contenu de la table users.
