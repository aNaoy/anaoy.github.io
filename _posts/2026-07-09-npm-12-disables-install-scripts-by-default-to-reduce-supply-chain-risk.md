---
title: 'npm 12 Disables Install Scripts by Default to Reduce Supply Chain Risk'
date: 2026-07-09
permalink: /posts/2026/07/09/npm-12-disables-install-scripts-by-default-to-reduce-supply-chain-risk/
tags:
- veille-cyber
- hackernews
---
# Renforcement de la sécurité de la chaîne d'approvisionnement dans npm 12

GitHub a publié npm 12, introduisant des changements majeurs visant à réduire les risques liés à la chaîne d'approvisionnement en logiciel, notamment en désactivant par défaut l'exécution automatique des scripts lors de l'installation et en restreignant l'usage des jetons d'accès granulaire (GAT).

### Points clés
*   **Désactivation des scripts :** Les scripts de cycle de vie (ex: `preinstall`, `postinstall`), les builds `node-gyp`, les dépendances Git et les dépendances distantes provenant d'URLs ne sont plus exécutés automatiquement.
*   **Sécurisation des jetons (GAT) :** Les jetons configurés pour contourner l'authentification à deux facteurs (2FA) ne pourront plus effectuer d'actions sensibles (gestion de compte ou d'organisation).
*   **Limitation de publication :** La publication directe via des jetons GAT est restreinte au profit d'une publication par étapes nécessitant une validation humaine 2FA.

### Vulnérabilités ciblées
Cet article ne référence pas de CVE spécifique, mais traite de **risques structurels** liés aux chaînes d'approvisionnement :
*   **Exécution de code malveillant :** Prévention de l'injection de code via des scripts post-installation frauduleux dans des packages tiers.
*   **Détournement de comptes/tokens :** Réduction du risque lié aux jetons de longue durée permettant le contournement du 2FA.
*   **Vol de jetons :** Limitation de l'exposition aux attaques par redirection de registre via des fichiers `.npmrc` corrompus.

### Recommandations
*   **Validation explicite :** Utiliser la commande `npm approve-scripts --allow-scripts-pending` pour examiner et autoriser manuellement les scripts nécessaires, puis valider la liste dans le fichier `package.json`.
*   **Transition vers OIDC :** Migrer les processus de publication automatisés vers le *Trusted Publishing* (OIDC) plutôt que d'utiliser des jetons de publication longue durée.
*   **Authentification interactive :** Privilégier les actions de gestion de compte et de sécurité via une interaction directe nécessitant une authentification à deux facteurs.
*   **Mise à jour :** Passer à la version 11.16.0 ou supérieure pour anticiper les avertissements de sécurité avant le déploiement complet des nouvelles politiques.

---
[Source](https://thehackernews.com/2026/07/npm-12-disables-install-scripts-by.html){:target="_blank"}
