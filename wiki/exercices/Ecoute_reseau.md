# Exercices - Écoute du réseau

# Quiz sur la théorie   

[Petit quiz sur l'écoute du réseau](https://forms.office.com/r/21wbTS7464)  


# Exercices obligatoires  

Pour ces exercices, vous aurez besoin des VM suivantes :  
- Kali  
- Metasploitable  

Assurez-vous que votre VM Kali est configuré pour le mode _promiscuous_.

## 1 - Ping

Démarrer la capture dans Wireshark.

Dans la VM Metasploitable, lancez un `ping 8.8.8.8`

Arrêtez la capture dans Wireshark.

Quel est le protocole utilisé?

Prenez un Echo (ping) request et trouvez sa réponse.

Quelle est l'adresse IP source de la requête? Quelle est sa destination?

## 2 - nmap

Démarrer la capture dans Wireshark.

Dans la VM Kali, lancez un nmap avec comme cible la VM Metasploitable.

Arrêtez la capture dans Wireshark.

Quel est le protocole utilisé?

Que ce passe-t'il lorsqu'un port est ouvert?

Que ce passe-t'il lorsqu'un port est fermé?

## 3 - Telnet

Démarrer la capture dans Wireshark.

Dans la VM Kali, connectez-vous à Metasploitable via telnet (user et pass : msfadmin)

Arrêtez la capture dans Wireshark.

Quel est le protocole utilisé?

Reconstituez la conversation telnet. Quelle est la fonction pour ça?

## 4 - HTTPS

Démarrer la capture dans Wireshark.

Dans la VM Kali, ouvrez une page Web avec Firefox : https://www.google.ca.

Arrêtez la capture dans Wireshark.

Quels sont les protocoles utilisés?

Pouvez-vous trouver les paquets utilisés pour HTTPS?


# Exercices optionnels  

Pour ces exercices, vous aurez besoin des VM suivantes :  
- Kali  
- Metasploitable  

## 5 - FTP  

Démarrer la capture dans Wireshark.

Dans la VM Kali, connectez-vous à Metasploitable via ftp (user et pass : msfadmin)

Parcourez les répertoires de Metasploitable avec les commandes `cd` et `ls`.

Arrêtez la capture dans Wireshark.

Quel est le protocole utilisé?

Pouvez-vous retrouver dans la capture de Wireshark le mot de passe saisi?

Pouvez-vous expliquer pourquoi le code utilisateur entré est écrit dans la capture comme `mmssffaaddmmiinn`?  

## 6 - OpenVAS

Démarrer la capture dans Wireshark.

Dans la VM Kali, démarrez un balayage avec OpenVAS.

Attendez quelques minutes...

Arrêtez la capture dans Wireshark.

Quels sont les protocoles utilisés?

## 7 - MySQL (Avancé seulement)  

Démarrer la capture dans Wireshark.

Dans la VM Kali, connectez-vous à Metasploitable via mysql (user root, mot de passe vide)

Faîtes un `SHOW DATABASES`

Arrêtez la capture dans Wireshark.

Quel est le protocole utilisé?

Pouvez-vous retrouver dans la capture de Wireshark le code utilisateur et le mot de passe saisis?

