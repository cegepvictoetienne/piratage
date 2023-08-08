La base de données PostGreSQL dans Kali est utilisée par Metasploit Framework pour conserver les espaces de travail.

Pour démarrer la base de données, ouvrir une fenêtre de terminal et entrer la commande suivante :

`systemctl start postgresql`

Pour valider que la BD fonctionne dans MSF :

`msfconsole`

`db_status`
