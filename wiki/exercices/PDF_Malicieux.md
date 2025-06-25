# Exercices - PDF Malicieux

# Quiz sur la théorie  

[Petit quiz sur les antivirus et pdf malicieux](https://forms.office.com/r/BP5zBu2nDM)  

# Exercice obligatoire  

## Installation d'Adobe Reader

Sur votre VM Windows XP, téléchargez et installez la version 9.3.4 d'Adobe Reader.

[Téléchargement d'Adobe Reader 9.3.4](../labo/9.3.4_AdbeRdr934_en_US.exe)

## Créer votre PDF malicieux

Sur votre machine Kali :

1. Trouvez le module pour la faille CVE:2010-2883.
2. Chargez le module et renseignez les options.
3. Trouvez le PAYLOAD pour se connecter avec Meterpreter.
4. Assignez le PAYLOAD au module.
5. Configurez le PAYLOAD.
6. Créez le PDF.
7. Transférez le PDF à votre machine Windows XP.

## Démarrer le serveur Meterpreter sur kali

Commencez l'écoute avec le module approprié de Metasploit. (Voir leçon 9)

## Ouvrir le PDF

Sur votre machine Windows XP, ouvrez le PDF. Ensuite, allez dans votre Kali et attendez le démarrage de la session.

## Migrer le processus Meterpreter.

1. Trouvez un processus sur la machine qui est au nom de l'utilisateur.
2. Migrer le processus.

## Essayer les commandes Meterpreter

Voici quelques commandes à essayer :

- `getsystem`
- `sysinfo`
- `screenshot`
- `idletime`
- `shutdown`
