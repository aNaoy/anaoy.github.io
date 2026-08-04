---
title: 'Massive ChainDrop npm supply-chain attack infects hundreds of packages'
date: 2026-08-04
permalink: /posts/2026/08/04/massive-chaindrop-npm-supply-chain-attack-infects-hundreds-of-packages/
tags:
- veille-cyber
- bleepingcomp
---
### Propagation massive de "ChainDrop" : une attaque par supply-chain sur npm

Une attaque par empoisonnement de la supply-chain logicielle, nommée **ChainDrop**, a compromis plus de 1 300 packages sur le registre npm, totalisant 2 milliards de téléchargements mensuels. Le vecteur d'attaque initial a été la compromission du compte GitHub d'un mainteneur du package populaire *Keyv*, permettant aux attaquants de publier des versions malveillantes via des workflows GitHub Actions légitimes, ce qui confère aux paquets une apparence de fiabilité (provenance valide).

**Points clés :**
*   **Fonctionnement :** Le ver utilise un script `preinstall` pour exécuter un "dropper" (`setup.mjs`), qui télécharge le runtime Bun pour lancer une charge utile d'infostealer (`Math_Symbol.js` ou `math_init.js`).
*   **Capacités :** Le malware est auto-réplicant (infecte d'autres packages lors de l'installation) et hautement intrusif. Il dérobe une vaste gamme de secrets : tokens GitHub/npm, identifiants AWS/Azure/GCP, clés privées, secrets Kubernetes, Vault, et bases de données.
*   **Exfiltration :** Les données volées sont chiffrées puis envoyées vers un dépôt GitHub public ou le domaine `npm-cache[.]com`.
*   **Vulnérabilités :** L'attaque exploite la confiance accordée aux workflows CI/CD automatisés et l'exécution automatique des scripts `preinstall` lors de `npm install`. *Note : Aucune CVE n'est associée à cette campagne, car il s'agit d'un abus de fonctionnalités légitimes plutôt que de l'exploitation d'une faille logicielle spécifique.*

**Recommandations :**
*   **Réponse immédiate :** Si un package infecté a été utilisé, considérez le poste de travail du développeur ou le runner CI/CD comme compromis.
*   **Remédiation :**
    *   Réinitialiser immédiatement tous les secrets (tokens, clés API, mots de passe) accessibles depuis l'environnement de développement ou de build.
    *   Reconstruire les systèmes à partir de sauvegardes saines ou les réinstaller intégralement.
    *   Auditer les journaux d'accès pour détecter toute activité non autorisée ou des commits suspects.
*   **Mesures préventives :**
    *   Appliquer des contrôles de provenance stricts et des mécanismes d'intégrité pour les dépendances.
    *   Utiliser des listes d'autorisation (allowlisting) pour les packages autorisés.
    *   Surveiller les indicateurs de compromission (IoC) fournis par les entreprises de sécurité (Wiz, Aikido, Socket, etc.).

---
[Source](https://www.bleepingcomputer.com/news/security/massive-chaindrop-npm-supply-chain-attack-infects-hundreds-of-packages/){:target="_blank"}
