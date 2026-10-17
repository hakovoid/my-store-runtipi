# BiblioBox

Gestionnaire de collection de mangas, BD, comics et livres. Il cherche tout seul les couvertures, les auteurs, l'éditeur, la date et le résumé de ton **édition française**, à partir de l'EAN du livre.

## Fonctionnalités principales

- **Une ligne par série**, qui se déplie pour montrer les tomes ; les tomes manquants sont signalés
- **BD, mangas, comics et livres**, avec un type d'album par tome (tome, one-shot, intégrale, coffret, hors-série)
- **Scan des codes-barres** : douchette, webcam ou appareil photo du téléphone
- **Couvertures et informations** de l'édition française (BnF, Google Books, Open Library, Amazon)
- **Collections par personne**, avec un « lu » par personne
- **Nouveautés** des séries en cours et tomes manquants
- **Favori « 📚 BiblioBox »** pour remplir une fiche depuis manga-news, Bubble ou Babelio
- Import de l'export CSV de Bubble, export CSV, sauvegardes automatiques
- Thème clair ou sombre, style Papier & Encre

## Configuration requise

- **Port** : 8080 (interne), exposé sur le port de votre choix
- **Mot de passe d'accès** : demandé à l'ouverture, un seul mot de passe pour tout le monde
- **Nom de domaine** (facultatif) : à renseigner si vous ouvrez BiblioBox par un nom de domaine
- **Clé Google Books** (facultative) : un quota de recherche à soi, au lieu du quota partagé

## Après l'installation

1. Ouvrez BiblioBox depuis Runtipi et connectez-vous avec le mot de passe choisi
2. **Menu → Importer** pour reprendre un export Bubble, ou ajoutez des tomes avec **Scanner** ou **+ Ajouter**
3. Cliquez sur **Chercher couvertures et résumés**

Pour reprendre une collection existante, arrêtez l'application, copiez le dossier `data` d'une ancienne BiblioBox dans le dossier de données de l'app Runtipi, puis redémarrez.

## Caméra et HTTPS

Les navigateurs n'autorisent la caméra (scan des codes-barres) et le favori depuis une page HTTPS que si BiblioBox est servie en HTTPS. En clair, par `http://adresse-ip:port`, tout marche sauf ces deux fonctions ; la douchette et la saisie à la main fonctionnent. Derrière un nom de domaine en HTTPS, tout marche.

## Ressources

- [Code source et documentation](https://github.com/hakovoid/BiblioBox)
