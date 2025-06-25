# Exercices - Détection d'intrusion 

# Quiz sur la théorie   

[Petit quiz de la détection d'intrusion](https://forms.office.com/r/VzpVFmG3hm)  

# Exercices obligatoires  


[snort]: ../labo/Installation_Snort_VirtualBox.md "Snort"

Vous aurez besoin de la machine virtuelle de snort :  [snort][]  

Assurez-vous que snort a sa carte réseau en _promiscuous_.

Vous aurez besoin de 3 VM : Kali, snort et Metasploit.  

## NMAP  

1. Créez une règle dans snort qui détecte un __NMAP Syn scan__  
2. À partir de Kali, balayez Metasploitable avec nmap  
3. Vérifiez que snort détecte bien le balayage   

## FTP avec user _root_  

1. Créez une règle dans snort qui détecte __FTP avec user root__  
2. À partir de Kali, connectez-vous à Metasploitable avec ftp et utilisateur _root_  (utilisez n'importe quel mot de passe, le but est de détecter la tentative de connexion)  
3. Vérifiez que snort détecte bien la tentative de connexion   


## Telnet avec login invalide  

1. Créez une règle dans snort qui détecte __Telnet avec login invalide__  
2. À partir de Kali, connectez-vous à Metasploitable avec telnet et n'importe quel utilisateur. (utilisez n'importe quel mot de passe, le but est de détecter la tentative de connexion)  
3. Vérifiez que snort détecte bien la tentative de connexion invalide  

# Exercices optionels  

## SSH 

1. Créez une règle dans snort qui détecte __une connexion au service ssh__  
2. À partir de Kali, connectez-vous à Metasploitable avec ssh (utilisateur : msfadmin, mot de passe : msfadmin) 
3. Vérifiez que snort détecte bien la connexion ssh  


## Nikto  

1. Créez une règle dans snort qui détecte un __balayage avec Nikto__  
2. À partir de Kali, balayez Metasploitable avec nikto  
3. Vérifiez que snort détecte bien le balayage   


