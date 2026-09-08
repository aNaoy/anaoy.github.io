---
title: 'Slim Spider Steals Crypto Custody Secrets From Brazilian Financial Institution'
date: 2026-09-08
permalink: /posts/2026/09/08/slim-spider-steals-crypto-custody-secrets-from-brazilian-financial-institution/
tags:
- veille-cyber
- hackernews
---
### Slim Spider : Une menace sophistiquée pour les infrastructures financières brésiliennes

Le groupe cybercriminel « Slim Spider » cible activement les institutions financières au Brésil depuis mars 2026. Ce groupe se distingue par une expertise avancée des environnements Cloud et des infrastructures de paiement instantané (Pix), utilisant des techniques sophistiquées pour dérober des actifs en cryptomonnaies et manipuler des transactions financières.

**Points clés :**
*   **Mode opératoire :** Incursions multi-étapes exploitant les métadonnées d'instances Cloud pour extraire des identifiants temporaires.
*   **Techniques d'évasion :** Utilisation de scripts Bash personnalisés, de bibliothèques natives comme OpenSSL (pour éviter les détections tierces) et de binaires imitant des outils système légitimes.
*   **Automatisation :** Utilisation de panneaux de contrôle dédiés pour l'analyse d'API (NEXUS), la reconnaissance de boîtes mail (Microsoft 365) et l'exécution de transferts Pix frauduleux en masse.
*   **Pivotement :** Compromission d'Azure DevOps pour déployer des implants malveillants directement au sein de clusters Kubernetes.

**Vulnérabilités et vecteurs d'attaque :**
*   **Exposition des métadonnées :** Accès aux instances Cloud via des requêtes de métadonnées non restreintes.
*   **Gestion des secrets :** Faiblesse dans la protection des identifiants stockés dans les gestionnaires de secrets Cloud.
*   **CI/CD :** Pipelines Azure DevOps compromis permettant le déploiement automatisé de logiciels malveillants.
*   **Backdoor spécifique :** Utilisation du malware « MikeDor », un implant basé sur Go, pour l'exfiltration de données et la surveillance active.

**Recommandations :**
*   **Sécurisation du Cloud :** Restreindre strictement l'accès aux points de terminaison des métadonnées (IMDS) et appliquer le principe du moindre privilège aux rôles Cloud.
*   **Surveillance des secrets :** Mettre en place une rotation fréquente des identifiants et utiliser des solutions de gestion de secrets avec audit strict.
*   **Intégrité des pipelines :** Sécuriser les environnements CI/CD (Azure DevOps/Kubernetes) par une authentification multi-facteurs (MFA) renforcée et une surveillance des activités anormales au sein des pipelines.
*   **Détection :** Monitorer l'exécution de commandes système suspectes (`sed`, `cast`) et les accès inhabituels vers les services de gestion de secrets ou les composants d'infrastructure de paiement.

---
[Source](https://thehackernews.com/2026/09/slim-spider-steals-crypto-custody.html){:target="_blank"}
