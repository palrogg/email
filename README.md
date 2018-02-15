# E-mails inutiles

Statistiques subjectives pour une chronique: les e-mails inutiles que je reçois, sur 31 jours.

## Marche à suivre

### 1. Réunir les e-mails au format mbox

Le script traite des courriels au format mbox.

C’est une famille de formats de stockage d'e-mails très courants. Elle est définie par la norme [rfc4155](https://tools.ietf.org/html/rfc4155).

Des clients comme Thunderbird et Apple Mail stockent les messages en respectant cette norme. D’autres comme Outlook permettent un export en mbox.

Plus simple: certains hébergeurs mail permettent de télécharger l’archive au format mbox. C’est notamment le cas de Gmail, à l’adresse [takeout.google.com](https://takeout.google.com/).

### 2. Sélectionner les données

Le script [1_mbox_reader.ipynb] lit les données du fichier 
