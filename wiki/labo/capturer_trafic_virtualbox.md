# Pour capturer le trafic d'une machine virtuelle dans VirtualBox

1- Dans le terminal, utiliser la commande suivante :

`VBoxManage modifyvm "metasploitable" --nictrace1 on --nictracefile1 /Users/etiennerivard/Documents/ftp.pcap`

2- Démarrer la VM avec la commande suivante :

`VirtualBoxVM -startvm metasploitable`

Références :
[https://www.virtualbox.org/wiki/Network_tips](https://www.virtualbox.org/wiki/Network_tips)
