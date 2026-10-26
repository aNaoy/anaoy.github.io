---
title: 'Microsoft 365 Token-Replay Attacks Compromise 97 Accounts at 79 Organizations'
date: 2026-10-26
permalink: /posts/2026/10/26/microsoft-365-token-replay-attacks-compromise-97-accounts-at-79-organizations/
tags:
- veille-cyber
- hackernews
---
### Campagne de « Token Spraying » contre Microsoft 365

Une campagne cybercriminelle sophistiquée a compromis 97 comptes au sein de 79 organisations en utilisant des attaques par « rejeu de jetons » (token replay). Contrairement aux attaques par force brute classiques, les attaquants utilisent des pages de hameçonnage de type *Adversary-in-the-Middle* (AitM) pour intercepter les jetons de session légitimes après le franchissement de l'authentification multifacteur (MFA).

**Points clés :**
*   **Méthodologie :** Les attaquants déploient des pages de connexion factices pour capturer les jetons d'accès. Ces jetons sont ensuite réutilisés pour accéder aux services Microsoft 365, contournant ainsi le besoin d'une seconde étape MFA.
*   **Persistance :** Une fois l'accès obtenu, les attaquants ajoutent leur propre application d'authentification ou enregistrent des appareils factices (« rogue devices ») dans Microsoft Entra ID pour maintenir un accès durable.
*   **Actions malveillantes :** Les attaquants créent des règles de messagerie dissimulées pour masquer les communications liées aux transactions financières (paie, dépôts) et utilisent les comptes compromis pour diffuser du spam.
*   **Origine :** L'infrastructure utilisée est liée à des services d'hébergement suspects, notamment le réseau associé à StarkRDP/exy[.]sh.

**Vulnérabilités :**
*   Bien qu'il ne s'agisse pas d'une vulnérabilité logicielle spécifique (CVE), l'attaque exploite la confiance accordée aux jetons de session valides après une authentification réussie.
*   Le flux de code d'appareil (*device-code phishing*) constitue un vecteur d'entrée majeur utilisé dans cette campagne.

**Recommandations :**
*   **Révision de sécurité :** Révoquer immédiatement les sessions actives, réinitialiser les mots de passe et auditer les méthodes MFA enregistrées ainsi que les appareils Entra ID.
*   **Audit de configuration :** Rechercher des règles de transfert ou de suppression automatique dans les boîtes de réception et inspecter les applications d'entreprise récemment ajoutées.
*   **Politiques d'accès conditionnel (CAP) :** Mettre en œuvre des politiques strictes exigeant le MFA pour tous les utilisateurs, toutes les applications cloud et tous les types d'applications clientes.
*   **Durcissement :** Restreindre ou bloquer le flux de code d'appareil via les politiques d'accès conditionnel pour limiter les vecteurs de phishing.

---
[Source](https://thehackernews.com/2026/10/microsoft-365-token-replay-attacks.html){:target="_blank"}
