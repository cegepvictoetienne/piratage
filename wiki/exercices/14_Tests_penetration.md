# Exercices - Tests de pénétration 

## Windows XP

Avec Kali et Windows XP :

Essayez ce que le professeur a démontré en classe. Avec Metasploit :  

1. Créez un espace de travail  
2. Balayez la VM Windows XP  
3. Lancez l'_exploit_ *ms08_067_netapi*

Essayez l'utilisation de Meterpreter :  

1. Créez un fichier sur Kali et téléversez-le sur Windows
2. Videz l'historique des événements
3. Naviguer à travers les répertoires
4. Cherchez un fichier nommé hosts
5. Affichez le contenu de hosts
6. Prenez un screenshot de l'écran de Windows
7. Ouvrez un shell


## Metasploitable

La section de Metasploitable requiert un peu de recherche. Voyez ceci comme un défi :

Défi 1 - Se connecter par Remote Shell (protocole RSH - Port 515)

Indices : module kali rsh-client, commande rlogin

Défi 2 - distccd - port 3632

Indices : module metasploit

Défi 3 - Tomcat, port 8180

Indices : module metasploit (scanner)

Ultime Défi (optionnel) - utiliser nfs pour se donner accès à ssh

Indices : nsf-common, showmount, mount, ssh-keygen
