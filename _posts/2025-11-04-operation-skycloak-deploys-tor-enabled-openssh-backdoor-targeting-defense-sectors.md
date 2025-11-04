---
title: 'Operation SkyCloak Deploys Tor-Enabled OpenSSH Backdoor Targeting Defense Sectors'
date: 2025-11-04
permalink: /posts/2025/11/04/operation-skycloak-deploys-tor-enabled-openssh-backdoor-targeting-defense-sectors/
tags:
- veille-cyber
- hackernews
---
## Opération SkyCloak : Une Porte Dérobée Sophistiquée Cible le Secteur de la Défense

Une campagne de cyberespionnage, baptisée Opération SkyCloak, utilise des courriels de phishing contenant des pièces jointes malveillantes pour déployer une porte dérobée persistante. Cette menace vise particulièrement les secteurs de la défense en Russie et en Biélorussie. Les courriels simulent des documents militaires pour inciter les victimes à ouvrir des fichiers ZIP.

L'infection se déclenche via un fichier raccourci Windows (LNK) qui lance une chaîne d'infection complexe. Celle-ci utilise PowerShell pour des vérifications d'environnement visant à détecter les environnements sandbox. Si ces vérifications sont réussies, le malware affiche un document PDF comme leurre et établit la persistance sur le système à l'aide d'une tâche planifiée nommée "githubdesktopMaintenance".

Le cœur de la menace réside dans l'utilisation d'OpenSSH, renommé pour se faire passer pour un exécutable légitime ("sshd.exe"), permettant ainsi aux acteurs de la menace d'établir un service SSH contrôlé par des clés autorisées pré-déployées. En plus du transfert de fichiers via SFTP, un deuxième service Tor personnalisé ("pinterest.exe") est configuré. Ce dernier utilise le protocole obfs4 pour masquer le trafic et crée un service caché sur le réseau Tor, se connectant à une adresse .onion de l'attaquant.

Ce mécanisme permet le transfert de port pour des services critiques tels que RDP, SSH et SMB, accordant un accès complet au système compromis via le réseau Tor, tout en assurant l'anonymat des attaquants. Le malware exfiltre ensuite des informations système et une URL .onion unique identifiant la machine compromise, permettant ainsi aux cybercriminels d'obtenir un accès à distance.

Bien que l'origine exacte de cette campagne soit encore inconnue, les similarités tactiques observées avec des activités d'espionnage liées à l'Europe de l'Est et une campagne antérieure attribuée à UAC-0125 suggèrent une cible gouvernementale et de défense.

**Points Clés :**

*   **Ciblage :** Secteurs de la défense en Russie et en Biélorussie.
*   **Méthode d'infection :** Courriels de phishing avec pièces jointes malveillantes (fichiers ZIP contenant un LNK).
*   **Technologie principale :** OpenSSH utilisé comme porte dérobée avec un service Tor personnalisé pour la communication C2.
*   **Obfuscation :** Utilisation de obfs4 pour masquer le trafic réseau.
*   **Persistance :** Tâches planifiées ("githubdesktopMaintenance").
*   **Accès :** Permet le transfert de fichiers (SFTP), RDP, SSH, SMB via le réseau Tor.
*   **Objectif :** Cyberespionnage et exfiltration de données.

**Vulnérabilités (sans CVE spécifiques mentionnées dans l'article) :**

*   Utilisation de OpenSSH comme vecteur de porte dérobée.
*   Exécution de code à distance via des fichiers LNK malveillants.
*   Contournement des défenses via des techniques d'obfuscation et d'évasion de sandbox.

**Recommandations :**

*   Sensibilisation accrue aux courriels de phishing, en particulier ceux utilisant des thèmes militaires.
*   Vérification rigoureuse des pièces jointes, même celles semblant légitimes.
*   Mise à jour et sécurisation des systèmes OpenSSH et de leurs configurations.
*   Surveillance des activités de réseau suspectes, notamment l'utilisation du réseau Tor pour des communications sortantes non autorisées.
*   Application de politiques de sécurité strictes concernant les tâches planifiées et l'exécution de scripts PowerShell.

---
[Source](https://thehackernews.com/2025/11/operation-skycloak-deploys-tor-enabled.html){:target="_blank"}
