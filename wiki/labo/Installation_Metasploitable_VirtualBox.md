# Installation de Metasploitable dans VirtualBox

Télécharger le vmdk de Windows XP via la page de téléchargement :

[Page de téléchargement](https://cegepvicto.sharepoint.com/:u:/s/Piratageethique/EVrPSZtUtX5KleUH_veBYQMBupRliViJ5GykQql_LJALmQ?e=1R31sI)

Télécharger le ZIP. **Extraire** les fichiers du zip.

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
