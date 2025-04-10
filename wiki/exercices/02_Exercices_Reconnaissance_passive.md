# Exercices - Reconnaissance passive

## Mise en situation - 1

Vous voulez en savoir plus sur votre professeur. Vous connaissez les informations suivantes :  

-  Son nom est Étienne Rivard  
-  Son courriel personnel est etienne@kerzo.ca  

Trouvez les informations suivantes :  

- Noms des membres de sa famille  
- Adresse civique en 2015  
- Adresse civique en 2020  
- Page de la maison modèle correspondant à l'adresse civique en 2020
- Numéro de téléphone
- Année de construction de sa maison actuelle (la même qu'en 2020)  
- Plus récent diplôme obtenu
- Endroit où travaille son épouse
- Endroit où travaille son fils
- Diplôme le plus récent de sa fille
- Publication scientifique  
- Endroit où il s'est marié  
- Combien d'années il a travaillé au Cégep de Victoriaville
- Qui a gagné la bourse ATE en 2024 et est pris en photo avec lui
- Code utilisateur sur GitHub
- Site de "bookmarks" personnel
- Instagram du chat de la famille


[Inscrivez vos réponses dans ce formulaire](https://forms.office.com/Pages/ResponsePage.aspx?id=JvVsnYGt-EanOqUHqvBs2h4e_CrnfMxFsMr2ZqveBNhURDRTVFZQMVpXRUdYV0JOQzNDUFk3VlpQMi4u)  

## Mise en situation - 2

Vous êtes dans une équipe de piratage éthique. Votre rôle est de faire la reconnaissance passive pour votre client. Le client est le Cégep de Victoriaville.

### 1 - Mode manuel

Commencer avec les outils manuels. Faire la recherche des sous-domaines avec NMMapper's Subdomain Finder.

Voir si vous pouvez trouver d'autres sous-domaines avec le rapport de Google (Google Certificate Transparency Report).

### 2 - Mode automatique

Dans Kali, utiliser l'outil `recon-ng`.

Étapes :  

1. Créer un espace de travail  
2. Ajouter le domaine principal à la base de données  
3. Installer et utiliser les différents modules pour la reconnaissance (certificate_transparency, whois_pocs, brute_hosts, recon/hosts-hosts/resolve)  
4. Générer un rapport en html  

Référence : [Cours 2 - Reconnaissance passive](../lecons/02_Reconnaissance_passive.md)
