# Metabolic Log

Journal alimentaire et sportif à saisie libre, analysé par un LLM, calibré sur un bilan sanguin personnel.

Les applications de suivi nutritionnel comptent des calories contre une cible générique. Metabolic Log inverse la logique : les cibles et les commentaires dérivent des marqueurs biologiques réels — foie, lipides, métabolisme — pas d'un objectif de poids abstrait.

## Fonctionnalités principales

- **Saisie libre** : texte ou photo d'assiette, analysée par un modèle de langage (macros, drapeaux nutritionnels, commentaire situé)
- **Évaluer avant de manger** : un avis sur un aliment envisagé, sans rien enregistrer, tenant compte des marges réellement restantes dans la journée
- **Bilan du jour** au format compte-rendu de laboratoire, interprété localement par un moteur de règles
- **Suivi d'activité** hebdomadaire sur un programme en 4 phases
- **Bilans sanguins** : saisie par photo (jusqu'à 8 pages), comparaison au bilan précédent, dérivation des repères alimentaires
- **Rapport pour le médecin**, exports CSV et sauvegarde JSON, tous produits localement
- **Chiffrement au repos** (SQLCipher) de la base de données
- **Accès protégé par mot de passe**, demandé à l'ouverture

## Configuration requise

- **Port** : 3000 (interne), exposé sur le port de votre choix
- **Mot de passe d'accès** : demandé à l'ouverture de l'application
- **Clé de chiffrement de la base** : générée automatiquement à l'installation, à sauvegarder précieusement — sans elle, la base est définitivement illisible
- **Au moins un fournisseur d'analyse** : clé API Anthropic, clé API OpenAI, ou une instance Ollama accessible sur le réseau

## Après l'installation

1. Accédez à Metabolic Log via l'interface Runtipi et connectez-vous
2. Renseignez votre profil (âge, taille, poids, cibles) dans « Profil et cibles »
3. Saisissez votre premier bilan sanguin dans « Bilans sanguins »
4. Cliquez « Adapter au dernier bilan » pour calibrer les repères alimentaires

## Confidentialité

Le contexte transmis au modèle lors de l'analyse d'un repas est volontairement générique (« transaminases élevées », jamais de valeur chiffrée) : les valeurs réelles du bilan sanguin ne quittent le poste que lors d'une dérivation explicite des repères, une poignée de fois par an, jamais lors de l'analyse quotidienne des repas.

## Avertissement

Les valeurs nutritionnelles sont des estimations produites par un modèle de langage, pas des mesures de laboratoire. Elles servent à observer une tendance, pas à établir un diagnostic. Toute décision médicale relève du médecin traitant.

## Ressources

- **Source** : [hakovoid/metabolic-log](https://github.com/hakovoid/metabolic-log)
