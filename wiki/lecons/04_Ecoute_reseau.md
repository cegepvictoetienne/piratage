# Écoute du réseau avec Wireshark

Wireshark est un analyseur de protocole réseau. Avec cet outil, nous pouvons collecter tous les paquets IP qui se transigent sur le réseau.

Dans notre laboratoire, Wireshark sera utilisé dans Kali. Normalement, VirtualBox gère le réseau comme un commutateur (_switch_). Le trafic réseau entre 2 machines ne peut pas être vu par une 3ème machine.

Ex:

Machine A : Windows XP  
Machine B : Metasploitable  
Machine C : Kali  

Quand la machine A communique avec la machine B, seulement la machine A et la machine B _voient_ les paquets. Ceux-ci sont invisibles pour la machine C.

Il y a cependant une manière de contourner ceci, pour que Kali puisse _voir_ le trafic des autres VM. C'est le mode _promiscuous_.

!!! figure "Dans les configurations de la VM Kali, dans la section Network, changez le Promiscuous Mode_ à Allow All"
    ![04-VirtualBox-Promiscuous-Mode](../images/2020/06/04-virtualbox-promiscuous-mode.png)

## Démarrer une écoute du réseau

!!! figure "Écran principal de Wireshark"
    ![04-wireshark-main-screen](../images/2020/06/04-wireshark-main-screen.png)

!!! figure "Pour démarrer l'écoute, double-cliquez sur eth0."
    ![04-wireshark-capture-screen](../images/2020/06/04-wireshark-capture-screen.png)
    1. Interface de filtre  
    2. Liste des paquets transmis  

Avant d'aller plus loin, disons que nous sommes allés sur la page principale de Google.

## Filtres

Une des premières choses qu'un ordinateur fait lorsque nous voulons accéder à une page Web et de faire un requête au serveur DNS.

!!! figure "Recherchons les paquets DNS dans notre capture"
    ![04-wireshark-dns-filter](../images/2020/06/04-wireshark-dns-filter.png)

Regardez les deux premières entrées :

La première montre notre ordinateur (192.168.40.4) fait une demande de requête DNS au serveur DNS (192.168.2.1). La seconde entrée montre la réponse du serveur DNS à notre ordinateur.

!!! figure "Pour trouver la réponse spécifique à une requête, on peut activer un filtre en quelques étapes"
    ![04-wireshark-dns-id-filter](../images/2020/06/04-wireshark-dns-id-filter.png)
    1. Cliquer sur la transaction dns  
    2. Dans la section Domain Name System (query), faire un clic droit sur l'item transaction id  
    3. Sélectionner le menu Prepare as filter  
    4. Sélectionner le menu Sélectionné  

Ce que ça donne est le filtre `dns.id==<id_transaction>`

!!! figure "Il est aussi possible de l'inscrire manuellement"
    ![04-wireshark-after-dns-id-filter](../images/2020/06/04-wireshark-after-dns-id-filter.png)

!!! figure "Pour voir les paquets qui sont reçus du serveur de Google, appliquons un différent filtre"
    `ip.src == 172.217.13.195`
    ![04-wireshark-ip-src-filter](../images/2020/06/04-wireshark-ip-src-filter.png)

!!! figure "Pour voir les paquets envoyés ET reçus du serveur de Google"
    `ip.src == 172.217.13.195 or ip.dst == 172.217.13.195`
    ![04-wireshark-ip-src-or-ip-dst](../images/2020/06/04-wireshark-ip-src-or-ip-dst.png)

Prendre note des 3 premières transactions avec le protocole TCP. On peut y voir clairement la négociation à 3 étapes (_3-way-handshake_) de TCP entre les deux intervenants.

À noter que `ip.addr == 172.217.13.195` est équivalent à `ip.src == 172.217.13.195 or ip.dst == 172.217.13.195`

Autres recherches possibles :

`tcp.port == 443`  
`data-text-lines contains "twiki"`  
`http.request.method == "GET"`  

## nmap

Qu'arrive-t'il lorsque nous utilisons la commande nmap?

Exécutons la commande suivante :

`sudo nmap -sS T4 192.168.40.7`

!!! figure "Résultat de nmap dans Wireshark"
    ![04-wireshark-after-nmap](../images/2020/06/04-wireshark-after-nmap.png)
    Disons que ce n'est pas discret!!!

## Nitko

Qu'arrive-t'il lorsque nous utilisons la commande nitko?

Exécutons la commande suivante :

`nitko -h 192.168.40.7`

!!! figure "Résultats de nitko dans Wireshark"
    ![04-wireshark-nitko](../images/2020/06/04-wireshark-nitko.png)
    Impossible de passer inaperçu!

## Protocoles insécures

Wireshark peut nous aider à espionner les victimes lorsqu'ils utilisent des protocoles non sécuritaires.

### FTP

!!! figure "Voici la transaction ftp"
    ![04-ftp-session](../images/2020/06/04-ftp-session.png)

!!! figure "Résultat de ftp dans Wireshark"
    ![04-wireshark-ftp](../images/2020/06/04-wireshark-ftp.png)
    Avez-vous trouvé le mot de passe utilisé?

### Telnet

!!! figure "Voici la transaction telnet"
    ![04-telnet-session](../images/2020/06/04-telnet-session.png)

!!! figure "Résultat de telnet dans Wireshark"
    ![04-wireshark-telnet](../images/2020/06/04-wireshark-telnet.png)
    Ce n'est pas très facile de voir ce qui se passe. Telnet envoie les touches appuyées une par une...

!!! figure "Une fonctionnalité de Wireshark est de recueillir la communication ou conversation avec sa fonction suivre le flux"
    ![04-wireshark-follow-stream-menu](../images/2020/06/04-wireshark-follow-stream-menu.png)

!!! figure "Résultat de suivre le flux"
    ![04-wireshark-follow-telnet-tcp-stream](../images/2020/06/04-wireshark-follow-telnet-tcp-stream.png)

!!! important  
    Prenez quelques minutes pour faire votre [cartographie](../outils/cartographie.md) de la leçon d'aujourd'hui!   

## Testez vos connaissances  

[Petit quiz sur l'écoute du réseau](https://forms.office.com/r/21wbTS7464)  
