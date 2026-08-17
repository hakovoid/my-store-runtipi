# my-store-runtipi

--- 

# Metabolic Log

**Journal alimentaire et sportif à saisie libre, analysé par un LLM, calibré sur un bilan sanguin personnel**

Les cibles et les commentaires dérivent des marqueurs biologiques réels — pas d'un objectif de poids générique.

## 🚀 Fonctionnalités principales

- **📝 Saisie libre** : texte ou photo d'assiette, analysée par IA (macros, drapeaux, commentaire situé)
- **🤔 Évaluer avant de manger** : un avis sans rien enregistrer, tenant compte des marges du jour
- **🧪 Bilan du jour** au format compte-rendu de laboratoire
- **🏃 Suivi d'activité** hebdomadaire sur un programme en 4 phases
- **🩸 Bilans sanguins** : saisie par photo, comparaison au précédent, repères alimentaires dérivés
- **📄 Rapport pour le médecin**, exports CSV/JSON, tous produits localement
- **🔒 Chiffrement au repos** (SQLCipher)

## 📋 Configuration requise

- **Port** : 3000 (interne)
- **Variables d'environnement** :
  - `DB_KEY` : clé de chiffrement de la base (générée automatiquement, obligatoire)
  - Au moins un fournisseur d'analyse : `ANTHROPIC_API_KEY`, `OPENAI_API_KEY`, ou `OLLAMA_URL`

## 🔧 Après l'installation

1. Accédez à Metabolic Log via l'interface Runtipi
2. Renseignez votre profil dans « Profil et cibles »
3. Saisissez votre premier bilan sanguin
4. Cliquez « Adapter au dernier bilan » pour calibrer les repères alimentaires

## 🔒 Confidentialité

Le contexte transmis au modèle lors de l'analyse d'un repas est volontairement générique, sans valeur chiffrée. Les valeurs réelles du bilan ne quittent le poste que lors d'une dérivation explicite des repères, pas lors de l'analyse quotidienne.

## 📚 Ressources

- **GitHub** : [hakovoid/metabolic-log](https://github.com/hakovoid/metabolic-log)
- **Version** : 0.19.0

---

# ByteStash

**Une solution moderne de stockage de snippets de code**

ByteStash est une application web élégante pour organiser et gérer vos snippets de code, construite avec React et Node.js.

## 🚀 Fonctionnalités principales

- **📝 Gestion de snippets** : Stockez et organisez vos snippets de code par langage et catégorie
- **👥 Comptes utilisateurs** : Support multi-utilisateurs avec authentification
- **🔐 Single Sign-On** : Intégration OIDC pour l'authentification SSO
- **🌐 Vue publique** : Partagez vos snippets publiquement
- **📤 Import/Export** : Sauvegardez et migrez vos snippets facilement
- **🏷️ Tags et catégories** : Organisez avec des tags personnalisés
- **🔍 Recherche avancée** : Trouvez rapidement vos snippets
- **🎨 Interface moderne** : UI React avec Tailwind CSS
- **🔗 API REST** : Documentation Swagger disponible

## 📋 Configuration requise

- **Port** : 5000 (par défaut)
- **Volumes** : Stockage persistant pour les snippets
- **Variables d'environnement** :
  - `JWT_SECRET` : Secret pour les tokens (obligatoire)
  - `TOKEN_EXPIRY` : Durée de validité des tokens (ex: 24h)
  - `ALLOW_NEW_ACCOUNTS` : Autoriser les nouvelles inscriptions

## 🔧 Après l'installation

1. Accédez à ByteStash via l'interface Runtipi
2. Créez votre premier compte (si autorisé)
3. Commencez à ajouter vos snippets de code
4. Organisez-les avec des tags et catégories

### ⚡ Configuration recommandée SANS comptes 

```sh
JWT_SECRET: dummy-secret
TOKEN_EXPIRY: 24h
ALLOW_NEW_ACCOUNTS: false
DEBUG: false
DISABLE_ACCOUNTS: true  ← LE PLUS IMPORTANT
```

## 🔒 Sécurité

- Générez un `JWT_SECRET` fort et unique
- Configurez `ALLOW_NEW_ACCOUNTS=false` après la création des comptes
- Utilisez HTTPS en production (géré par Runtipi)
- Activez le SSO pour une authentification centralisée

## 📚 Ressources

- **GitHub** : [jordan-dalby/ByteStash](https://github.com/jordan-dalby/ByteStash)
- **Documentation** : [Wiki ByteStash](https://github.com/jordan-dalby/ByteStash/wiki)
- **Version** : 1.5.0

## 💡 Conseils d'utilisation

- Utilisez des tags descriptifs pour faciliter la recherche
- Exportez régulièrement vos snippets pour backup
- Explorez l'API via l'interface Swagger
- Marquez les snippets utiles comme publics pour les partager
