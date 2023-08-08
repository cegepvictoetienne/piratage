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
[Registre des entreprise (Québec)](http://www.registreentreprises.gouv.qc.ca/fr/default.aspx)  |  Donne de l'information sur l'entreprise, incluant le nom du propriétaire et possiblement des adresses
[Cadastre du Québec](https://appli.mern.gouv.qc.ca/infolot/) | Consultation du cadastre du Québec  
[CanLII](https://www.canlii.org/fr/)  |  Tous les documents des tribunaux canadiens  
[OSINT Framework](https://osintframework.com/)  |  Une grande quantité d'outils d'intelligence du domaine public  

## Recherche de sous-domaines

Souvent, les sous-domaines sont des serveurs dans la DMZ de l’entreprise, bons points d’entrées dans le réseau.

Outils utilisés :

[DNS Dumpster](https://dnsdumpster.com/)

[NMMapper's Subdomain Finder](https://www.nmmapper.com/sys/tools/subdomainfinder/)

## Recherche par certificats émis

Lorsqu'une compagnie veut protéger les communications d'un serveur, elle achète des certificats. L'information est publique.

[Google Certificate Transparency Report](https://transparencyreport.google.com/https/certificates?hl=en)

Pour trouver l'adresse IP du nom de domaine :

`nslookup aeti.cegepvicto.ca`

Pour trouver de l'information sur le propriétaire de l'adresse IP :

`whois 206.167.10.37`

Pour avoir plus d'information, censys.io peut aider :

[censys.io search](https://censys.io/ipv4)

## Recherche de surfaces d'attaque avec Google Dorks

Grâce à des recherches dans Google, vous pouvez trouver des services ou des documents qui peuvent aider à découvrir les surfaces d'attaque.

[Google Dorks Database](https://www.exploit-db.com/google-hacking-database)

Ex:

`site:*.cegepvicto.ca intext:"Welcome to JIRA" "Powered by a free Atlassian Jira community"`

`site:*.ca intitle:"index of"`

## SpiderFoot

SpiderFoot est un outil qui automatise la reconnaissance passive. Pour l'utiliser :

`cd /usr/share/spiderfoot`

`python3 ./sf.py -l 127.0.0.1:5009`

Ouvrir le fureteur de Kali à cette adresse : http://127.0.0.1:5009

## Recon-ng

Recon-ng est une plateforme modulaire pour la reconnaissance. Basée sur les mêmes principes que MetaSploit, cet plateforme regroupe beaucoup d'outils pour aider à faire de la reconnaissance.

Pour démarrer :

`recon-ng`

L'outil recueille ses résultats dans des espaces de travail. Pour créer un espace, par exemple pour le cégep :

`workspaces create cegep`

la commande **db** permet d'interagir avec la base de données de l'espace de travail. Par exemple, pour ajouter le domaine du cégep :

`db insert domains`

Renseigner les champs :

`domain (TEXT) : cegepvicto.ca`

`Note (TEXT) : Cégep de Victoriaville`

Les modules de recon-ng sont accessibles via le marketplace.

Pour rechercher un module :

`marketplace search domains`

Retourne la liste des modules relatifs aux domaines.

Pour installer un module :

`marketplace install certificate_transparency`

Pour utiliser un module :

`modules load certificate_transparency`

Pour avoir de l'information sur le module :

`info`

Commencer par voir la liste des options :

`options list`

Assigner une variable :

`options set SOURCE cegepvicto.ca`

Exécuter le module :

`run`

Avec le module certificate_transparency, la découverte des actifs (HOSTS) ajoute les éléments dans la BD. Pour voir la liste des HOSTS :

`show hosts`

Pour faire le suivi de notre reconnaissance, utiliser la commande suivante :

`dashboard`

Voici quelques modules intéressants :

- whois_pocs
- brute_hosts
- recon/hosts-hosts/resolve

Recon-ng permet de faire des rapports :

Module: reporting/html

## Recherche de surfaces d'attaque en analysant le code source de pages web

Ex: [Site de Christiane](https://christianelagace.com)

Dans le code source, on peut voir :

`wp-content`

C'est un indicatif que le site est fait avec WordPress.

!!! important  
    Prenez quelques minutes pour faire votre [cartographie](../outils/cartographie.md) de la leçon d'aujourd'hui!   

## Testez vos connaissances  

[Petit quiz sur la reconnaissance passive](https://forms.office.com/r/7qNdDYPMpc)  

## Lectures supplémentaires

[Outils d'intelligence ouverte - OSINT](https://securitytrails.com/blog/osint-tools)  
[Tutoriel de Recon-ng](https://warroom.rsmus.com/recon-ng-tutorial/)  
[Autres outils de recherche de sous-domaines](https://securitytrails.com/blog/subdomain-scanner-find-subdomains)   
[Tutoriel Google Dorks et Hacks](https://myhackingworld.com/google-hacking-and-google-dorking-basics/)   
