# E-mails inutiles

Statistiques subjectives pour une chronique: les e-mails inutiles que je reçois, sur 31 jours.

## Marche à suivre

### 1. Réunir les e-mails au format mbox

Le script traite des courriels au format mbox.

C’est une famille de formats de stockage d'e-mails très courants. Elle est définie par la norme [rfc4155](https://tools.ietf.org/html/rfc4155).

Des clients comme Thunderbird et Apple Mail stockent les messages en respectant cette norme. D’autres comme Outlook permettent un export en mbox.

Plus simple: certains hébergeurs mail permettent de télécharger l’archive au format mbox. C’est notamment le cas de Gmail, à l’adresse [takeout.google.com](https://takeout.google.com/).

### 2. Sélectionner les données

Le script [1_mbox_reader.ipynb](1_mbox_reader.ipynb) lit les données d’un fichier mbox, sélectionne les données par date et par colonne et les sauvegarde sous la forme de deux tableaux:
* received.csv (tous les messages, spam compris, sauf les messages envoyés)
* sent.csv  (messages envoyés)

Il s'agit d'un «notebook» (code mêlé de texte) utilisant le langage Python. Si vous n'avez pas Jupyter Notebook, le logiciel open source Anaconda (licence BSD) permet de l'installer facilement [voir les instructions sur jupyter.org](https://jupyter.org/install).

Les détails sont expliqués dans le script.

### 3. Analyser les données

On est loin de l'échantillon représentatif et de l'analyse scientifique. Mais le script [2_email_rater.ipynb](2_email_rater.ipynb) classe les e-mails et génère une série de résultats. A adapter en fonction de votre méthode de tri.
