# Tests de pénétration

Les tests de pénétration sont effectués pour trouver la faille de la cible et en prendre contrôle.

Dans Kali, nous utiliserons Metasploit.

## Exploits

Comme mentionné précédemment, les pirates utilisent les faiblesses de la cible pour en prendre contrôle. C'est donc l'exploitation d'une vulnérabilité.

Dans Metasploit, l'exploitation des vulnérabilités se fait à l'aide de modules de type _exploits_.  

Pour rechercher un _exploit_, utiliser la commande suivante :  

`search type:exploit`

![14-msfconsole-search-exploit](../images/2020/06/14-msfconsole-search-exploit.png)

Regardons quels services sont actifs sur la cible :  

`db_nmap -sS 192.168.40.5`

![14-db_nmap-windowsxp](../images/2020/06/14-db-nmap-windowsxp.png)

Le port 445 correspond au service SMB. Regardons quel _exploit_ peut être utilisé :

`search smb type:exploit os:windows`  

![14-search-exploit-smb-windows](../images/2020/06/14-search-exploit-smb-windows.png)

Il y a plusieurs _exploits_ possibles.

Essayons quelques uns :  

![14-exploit-ms13_071_theme](../images/2020/06/14-exploit-ms13-071-theme.png)

La cible de cet _exploit_ semble être pour Windows XP SP3. Notre cible semble avoir Windows XP SP3 aussi.  

Regardons les infos :  

`info`

![14-exploit-ms13_071](../images/2020/06/14-exploit-ms13-071.png)

Ce module requiert l'installation d'un thème sur le poste... Continuons à chercher :  

![14-exploit-ipass-pipe-exec](../images/2020/06/14-exploit-ipass-pipe-exec.png)

Et son info :  

![14-exploit-ipass-pipe-info](../images/2020/06/14-exploit-ipass-pipe-info.png)

Essayons-le :

![14-exploit-ipass-pipe-exec-run](../images/2020/06/14-exploit-ipass-pipe-exec-run.png)

Cet _exploit_ n'a pas marché, passons au suivant :  

??? note "Exploit qui marche en Windows, mais pas sur MacOS."
    ![14-exploit-ms08-067-info](../images/2020/06/14-exploit-ms08-067-info.png)  
    ![14-exploit-ms08-067-detail](../images/2020/06/14-exploit-ms08-067-detail.png)  
    Lançons l'exécution :  
    ![14-exploit-ms08-067-success](../images/2020/06/14-exploit-ms08-067-success.png)  
    C'est un succès!!!

??? note "Exploit qui marche en MacOS"  
    ![ms17_010_psexec_info](../images/ms17_010_psexec_info.png)  
    ![ms17_010_psexec_detail](../images/ms17_010_psexec_detail.png)  
    Lançons l'exécution :  
    ![ms17_010_psexec_success](../images/ms17_010_psexec_success.png)  
    C'est un succès!!!  

## Meterpreter

Meterpreter est un _payload_ qui utilise un mécanisme d'injection de DLL en mémoire et donne un puissant outil qui roule sur le système de la victime.

Pour commencer, il y a une aide contextuelle dans Meterpreter :

`help`

![14-meterpreter-help](../images/2020/06/14-meterpreter-help.png)

`background`

Permet de retourner à Metasploit. Pour revenir à la session Meterpreter, utiliser

`sessions -i 1`

![14-meterpreter-background](../images/2020/06/14-meterpreter-background.png)

`cat`

Pour afficher le contenu d'un fichier :

![14-meterpreter-cat](../images/2020/06/14-meterpreter-cat.png)

`cd` pour changer de répertoire :

![14-meterpreter-cd](../images/2020/06/14-meterpreter-cd.png)

`pwd` indique le répertoire courant :  

![14-meterpreter-pwd](../images/2020/06/14-meterpreter-pwd.png)

`clearev` vide les historiques de Windows (Application, Système et sécurité)

_Event Viewer_ avant le ménage :  

![14-windowsxp-event-viewer-before](../images/2020/06/14-windowsxp-event-viewer-before.png)

Lançons le ménage :  

![14-meterpreter-clearev](../images/2020/06/14-meterpreter-clearev.png)

_Event Viewer_ après le ménage :

![14-windowsxp-event-viewer-after](../images/2020/06/14-windowsxp-event-viewer-after.png)

`download` pour télécharger un fichier de la machine cible

![14-meterpreter-download](../images/2020/06/14-meterpreter-download.png)

`execute` Démarre une commande sur la cible

![14-meterpreter-execute](../images/2020/06/14-meterpreter-execute.png)

`ls` Voir le contenu du répertoire courant

![14-meterpreter-ls](../images/2020/06/14-meterpreter-ls.png)

`ps` Voir les processus qui roulent sur la cible  

![14-meterpreter-ps](../images/2020/06/14-meterpreter-ps.png)

`search` Peut chercher à travers tout le système de fichier

![14-meterpreter-search](../images/2020/06/14-meterpreter-search.png)

`shell` Pour avoir une ligne de commande de Windows (bon vieux DOS)

![14-meterpreter-shell](../images/2020/06/14-meterpreter-shell.png)

`upload` Pour téléverser un fichier vers la cible

![14-meterpreter-upload](../images/2020/06/14-meterpreter-upload.png)

Résultat :

![14-windowsxp-upload-result](../images/2020/06/14-windowsxp-upload-result.png)

`screenshot` Prend une photo de l'écran de la victime

![14-meterpreter-screenshot](../images/2020/06/14-meterpreter-screenshot.png)

Résultat :  

![14-windowsxp-screenshot](../images/2020/06/14-windowsxp-screenshot.png)

`reboot` Redémarre le système de la cible


## Testez vos connaissances  

[Petit quiz sur les tests de pénétration](https://forms.office.com/r/6AiAhEjLid)  
