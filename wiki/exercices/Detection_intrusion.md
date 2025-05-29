# Exercices - Détection d'intrusion 

[snort]: ../labo/Installation_Snort_VirtualBox.md "Snort"

Vous aurez besoin de la machine virtuelle de snort :  [snort][]  

Assurez-vous que snort a sa carte réseau en _promiscuous_.

Vous aurez besoin de 3 VM : Kali, snort et Metasploit.  

## Reproduire les règles vues dans le cours

Ajoutez les règles vues dans la leçon et testez-les :  

1. NMAP Syn scan
2. FTP avec user root  
3. Telnet avec login invalide

## Créer vos propres règles et les tester   

1. Détecter tout essai de connexion à SSH
2. Détecter une reconnaissance avec Nikto  
