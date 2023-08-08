# Installation de Kali Linux dans VirtualBox

## Installation de VirtualBox

Télécharger VirtualBox : [VirtualBox downloads](https://www.virtualbox.org/wiki/Downloads)

Télécharger les extensions de VirtualBox (même lien)

## Créer le réseau interne de notre laboratoire

Notre laboratoire virtuel doit permettre à toutes les machines virtuelles de communiquer entre elles. Ce sera fait avec un réseau NAT (nat network).

Dans une fenêtre de commande :

Allez dans le répertoire de VirtualBox :

`cd \Program Files\Oracle\VirtualBox`

Exécutez la commande :  

`VBoxManage natnetwork add --netname cegep --network "192.168.40.0/24" --enable --dhcp on`

## Installation de Kali Linux

Aller à la page de téléchargement de Kali :

[Kali Linux Downloads](https://www.kali.org/downloads/)

Sélectionner la version Virtual Machine pour VirtualBox 64bits.

## Actions Post-Installation

Installer les outils VM :  

`sudo apt-get install open-vm-tools`  

Activer PostgreSQL au démarrage :

`sudo systemctl enable postgresql`
