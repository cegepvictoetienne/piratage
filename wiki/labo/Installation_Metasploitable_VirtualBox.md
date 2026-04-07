# Installation de Metasploitable dans VirtualBox

Télécharger le vmdk de Windows XP via la page de téléchargement :

[Page de téléchargement](https://cegepvicto.sharepoint.com/sites/Piratageethique/Documents%20partages/Forms/AllItems.aspx?id=%2Fsites%2FPiratageethique%2FDocuments%20partages%2FVM&viewid=28158d5b-d870-4d75-9721-77bd58ef9523)

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
