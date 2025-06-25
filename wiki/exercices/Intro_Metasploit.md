# Exercices - Intro Metasploit


# Quiz sur la théorie   

[Petit quiz sur Metasploit](https://forms.office.com/r/Qkan3UqXan)  


Pour ces exercices, vous aurez besoin de Kali et Metasploitable.

# Exercices obligatoires  

Dans Kali :
1. Ouvrez le terminal.  
2. Démarrez PostGreSQL.  
3. Initialisez la BD de Metasploit.  
4. Démarrez la console `msfconsole`.  
3. Créez un espace de travail nommé **cegep**.  
4. Avec **db_nmap**, balayez Metasploitable.  
5. Avec le auxiliary/scanner/portscan/tcp, balayez Metasploitable.   
6. Balayez pour les mots de passe de MySQL.   
7. Allez extraire le hashdump. (Suivez les étapes de la [leçon](../lecons/Intro_Metasploit.md))  

# Exercice optionnel (avancé)

Objectif de l'exercice : Obtenir le fichier /etc/passwd de Matasploit, via MySQL.  

Dans la console metasploit, utiliser le module `auxiliary/admin/mysql/mysql_sql`. 

Dans les options, utilisez la commande SQL suivante : `SELECT LOAD_FILE('/etc/passwd')`  


