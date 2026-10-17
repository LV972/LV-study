# LV-study — Classeur de révision

Un site simple pour réviser : on crée des matières, on écrit des fiches et des cours, on ajoute des PDF ou des images, et on se teste avec des QCM générés automatiquement.

Site en ligne : https://lv972.github.io/LV-study/

## Fonctionnalités

| Fonction | Description |
|---|---|
| Matières | Un nom et une couleur par matière |
| Fiches et cours | Éditeur de texte pour écrire ou coller son contenu |
| PDF et images | Ajout de fichiers (30 Mo maximum chacun) ; le texte des PDF est lu par le site |
| Générer une fiche | Résumé automatique à partir d'un PDF (titres, définitions, phrases importantes) |
| QCM | Questions à choix multiple créées à partir d'une fiche, avec score |
| Recherche | Recherche dans tous les cours et fiches du profil actif |
| Thème | Mode clair ou sombre |
| Sauvegarde | Export et import du contenu en texte |

## Les trois profils

Le site est partagé par trois personnes : **LE**, **LY** et **SA**.

| Règle | Détail |
|---|---|
| Choix du profil | Un écran « Qui est-ce ? » s'affiche à l'ouverture, tant qu'aucun profil n'est choisi |
| Données séparées | Chaque profil a ses propres matières, fiches, cours, QCM et PDF |
| Changer de profil | Bouton avec les initiales du profil, en haut à droite |
| Mémorisation | Le dernier profil choisi est retenu sur l'appareil |
| Données d'avant les profils | Reprises une seule fois par le **premier profil choisi** |

## Où sont enregistrées les données

Tout est stocké **dans le navigateur de l'appareil** (pas de serveur ni de compte).

| À savoir | Conséquence |
|---|---|
| Par appareil et par navigateur | LE sur un téléphone et LE sur un ordinateur n'ont pas les mêmes fiches |
| Par adresse du site | Un autre domaine (ex. ancien site Netlify) a ses propres données |
| Effacer les données du navigateur | Supprime les fiches : pense à sauvegarder |
| Les profils ne sont pas protégés | Il n'y a pas de mot de passe, n'importe qui peut choisir n'importe quel profil |

### Sauvegarder et restaurer

Sur la page d'accueil, section **Sauvegarde** :

1. **Copier la sauvegarde** : copie le contenu du profil actif (cours et fiches) en texte.
2. Pour restaurer : choisis le bon profil, colle le texte dans la zone d'import (ou choisis le fichier), puis clique sur **Importer**.

Les PDF et images ne sont pas inclus dans la sauvegarde : il faut les rajouter.

## Structure du dépôt

```
LV-study/
├── index.html            Le site entier (HTML, CSS et JavaScript)
├── .nojekyll             Évite un blocage de GitHub Pages
└── vendor/
    └── pdfjs/
        ├── pdf.min.js          Lecteur de PDF (pdf.js)
        ├── pdf.worker.min.js
        └── LICENSE.txt         Licence Apache 2.0 de pdf.js
```
## Crédits

- Lecteur de PDF : [pdf.js](https://mozilla.github.io/pdf.js/) de la Mozilla Foundation, sous licence Apache 2.0.
