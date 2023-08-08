# Installation de Metasploitable dans VirtualBox

Aller à la page de téléchargement de Metasploitable :

[Metasploitable Download](https://sourceforge.net/projects/metasploitable/)

Télécharger le ZIP. Extraire les fichiers du zip.

Copier le fichier **Metasploitable.vmdk** dans votre dossier VirtualBox.

Configurations de VirtualBox :

General :

Type : Linux

Version : Debian (64-bit)

Memory Size : 1024 MB

Processor : 1 CPU

Hard disk : Use an existing virtual hard disk file

Sélectionner le fichier **Metasploitable.vmdk**.

Une fois la machine virtuelle créée :

Display :

Video Memory : 16 MB

Scale Factor : 200%

Graphics Controller : VMSVGA

Network :

Attached to : NAT Network

Name : cegep

Démarrer la VM. Metasploitable est installé et fonctionnel.
