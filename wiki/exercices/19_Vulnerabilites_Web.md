# Exercices - Vulnérabilités Web 

L'ensemble des exercices de ce cours utilise une application Web nommée _Damn Vulnerable Web Application_ ou DVWA. C'est une application avec des vulnérabilités pour tester notre habileté à les exploiter.  

## Exécution de commandes  


Dans DVWA, aller dans la section _Command Execution_.

Faites les actions suivantes :  

1. Voir le contenu du répertoire courant
2. Voir le contenu du répertoire /etc
3. Voir la version de linux  
4. Créer une nouvelle page Web qui affiche votre nom et afficher-la

## Attaque avec une force brute  

Avec BurpSuite, essayer de cracker le mot de passe de la page Brute Force de DVWA.

Utiliser cette liste d'utilisateurs :
```
admin  
administrator  
gordonb  
smithy  
lucp  
lucieng  
```

Utiliser cette liste de mots de passe :

```  
charley  
abc123  
password   
qwerty  
123456  
letmein  
```

Quelles combinaisons avez-vous trouvé?

## Cross Site Scripting

1. Aller sur la page de XSS (stored) dans DVWA.  
2. Écrire le payload dans le message pour afficher une alerte qui affiche votre nom.  
3. Recharger la page, qu'arrive-t'il?

## Upload  

1. Créer un fichier avec un payload à l'aide de MSFVenom, pour avoir un shell meterpreter en php  
2. Téléverser votre payload
3. Exécuter le payload
4. Connectez-vous avec Metasploit
