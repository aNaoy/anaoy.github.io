---
title: 'Official SAP npm packages compromised to steal credentials'
date: 2026-04-30
permalink: /posts/2026/04/30/official-sap-npm-packages-compromised-to-steal-credentials/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de la chaîne d'approvisionnement SAP via npm

Des attaquants (probablement le groupe **TeamPCP**) ont compromis quatre paquets npm officiels de SAP afin d'exfiltrer des identifiants et des jetons d'authentification sur les machines des développeurs et au sein des environnements CI/CD.

#### Points clés
*   **Vecteur d'attaque :** Injection d'un script `preinstall` malveillant dans des paquets légitimes. Ce script télécharge et exécute un outil d'exfiltration de données (`execution.js`) via le runtime Bun.
*   **Capacités du malware :**
    *   Vol d'identifiants (GitHub, npm, AWS, Azure, GCP, Kubernetes, SSH).
    *   Extraction de secrets directement dans la mémoire vive des processus CI/CD, contournant le masquage des journaux.
    *   Auto-propagation en modifiant d'autres dépôts accessibles via les jetons volés.
    *   Utilisation de dépôts GitHub publics pour l'exfiltration et de messages de commit comme "dead-drop" pour recevoir des instructions.
*   **Paquets impactés (versions dépréciées) :**
    *   `@cap-js/sqlite` v2.2.2
    *   `@cap-js/postgres` v2.2.2
    *   `@cap-js/db-service` v2.10.1
    *   `mbt` v1.2.48

#### Vulnérabilités
Bien qu'aucune CVE spécifique ne soit associée à cette attaque, le vecteur principal est une **compromission de compte/jeton de publication npm** (possiblement via une mauvaise configuration de CircleCI), exploitant la confiance accordée aux paquets officiels de la chaîne d'approvisionnement logicielle.

#### Recommandations
*   **Mise à jour immédiate :** Vérifier l'utilisation des versions listées ci-dessus et migrer vers des versions sécurisées si disponible.
*   **Réinitialisation des accès :** En cas d'utilisation des versions compromises, révoquer et renouveler immédiatement tous les jetons (GitHub, npm, cloud) et clés SSH présents sur les machines ou dans les pipelines CI/CD potentiellement exposés.
*   **Audit CI/CD :** Revoir les configurations des secrets et des environnements d'intégration continue pour limiter l'exposition en mémoire.
*   **Surveillance :** Inspecter l'activité des dépôts GitHub pour détecter toute création de dépôts inhabituels portant la mention « A Mini Shai-Hulud has Appeared ».

---
[Source](https://www.bleepingcomputer.com/news/security/official-sap-npm-packages-compromised-to-steal-credentials/){:target="_blank"}
