---
title: 'Identity Visibility in 2026: The Foundation of Identity Security'
date: 2026-09-19
permalink: /posts/2026/09/19/identity-visibility-in-2026-the-foundation-of-identity-security/
tags:
- veille-cyber
- hackernews
---
### La visibilité des identités : pilier de la sécurité moderne

La gestion des identités (IAM) ne peut plus se limiter à la configuration théorique des accès. La multiplication des environnements cloud, des comptes locaux et des identités non-humaines a créé une "matière noire" de l'identité, échappant aux contrôles centralisés et devenant une cible privilégiée pour les attaquants utilisant des identifiants légitimes.

#### Points clés
*   **Intention vs Exécution :** L'IAM définit les politiques (intention), mais seule l'analyse au niveau des applications et de l'infrastructure révèle l'usage réel des accès (exécution).
*   **Élargissement de la surface d'attaque :** Les menaces reposent désormais sur le détournement de jetons, le mouvement latéral via des relations de confiance complexes et l'exploitation d'identités machines/non-humaines (comptes de service, API keys) souvent dépourvues de cycle de vie.
*   **Fragmentation multicloud :** Chaque fournisseur (AWS, Azure, Google Cloud, SaaS) utilise ses propres modèles, rendant impossible une vue unifiée sans normalisation des données.
*   **Approche Zero Trust :** La vérification continue nécessite une visibilité constante sur le contexte, les comportements et les droits effectifs (et non nominaux).

#### Vulnérabilités courantes
L'article souligne l'exploitation des failles suivantes :
*   **Utilisation de comptes légitimes (Valid Accounts - T1078) :** Exploitation du phishing et du vol de jetons.
*   **Privilèges excessifs :** Droits cumulés via des groupes imbriqués ou des relations de confiance inter-comptes.
*   **Identités "orphelines" :** Comptes sans propriétaire attitré, sans expiration et souvent sans MFA (Multi-Factor Authentication).

#### Recommandations stratégiques
Pour mettre en place un programme de visibilité efficace, les organisations doivent suivre ces étapes :

1.  **Découverte directe :** Ne pas se contenter des logs du fournisseur d'identité (IdP). Collecter les données directement depuis les applications et l'infrastructure pour identifier les comptes locaux et non répertoriés.
2.  **Cartographie des accès effectifs :** Analyser les relations réelles (liens entre entités, permissions héritées) plutôt que de se fier uniquement aux catalogues de rôles.
3.  **Assignation de propriété :** Chaque identité (humaine ou machine) doit être rattachée à un responsable humain et comporter une date d'expiration ou une politique de rotation.
4.  **Analyse comportementale :** Établir des lignes de base pour distinguer l'activité normale de l'automatisation des comportements suspects des attaquants.
5.  **Priorisation des risques :** Se concentrer initialement sur les "joyaux de la couronne" (applications critiques) et sur les comptes à haut risque (accès en écriture en production sans MFA).

---
[Source](https://thehackernews.com/2026/09/identity-visibility-in-2026-foundation.html){:target="_blank"}
