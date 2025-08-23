---
title: 'Chinese Hackers Murky, Genesis, and Glacial Panda Escalate Cloud and Telecom Espionage'
date: 2025-08-23
permalink: /posts/2025/08/23/chinese-hackers-murky-genesis-and-glacial-panda-escalate-cloud-and-telecom-espionage/
tags:
- veille-cyber
- hackernews
---
**Escalade de l'espionnage chinois dans le Cloud et les Télécoms**

Des acteurs de la cyberespionnage liés à la Chine intensifient leurs activités ciblant les environnements cloud et le secteur des télécommunications. Ces groupes exploitent des vulnérabilités connues et nouvelles, ainsi que des relations de confiance, pour obtenir un accès initial aux réseaux d'entreprise et collecter des renseignements.

**Points Clés :**

*   **Murky Panda (Silk Typhoon)** : Ce groupe, connu pour ses exploits de vulnérabilités sur Microsoft Exchange Server, cible désormais la chaîne d'approvisionnement informatique pour gagner un accès initial. Il abuse également des relations de confiance entre partenaires et clients cloud pour pénétrer dans les environnements SaaS et se déplacer latéralement. L'objectif principal semble être la collecte de renseignements, notamment par l'accès aux e-mails.
*   **Genesis Panda** : Cet acteur utilise l'infrastructure cloud pour l'exfiltration de données et cible les comptes des fournisseurs de services cloud afin d'élargir son accès et d'établir des mécanismes de persistance. Il montre un intérêt constant pour les systèmes hébergés dans le cloud afin d'utiliser le plan de contrôle cloud pour le mouvement latéral, la persistance et l'énumération.
*   **Glacial Panda** : Ce groupe cible spécifiquement le secteur des télécommunications, exploitant des vulnérabilités sur les serveurs exposés sur Internet et les systèmes Linux, y compris les anciennes distributions. Il utilise des techniques "living-off-the-land" et déploie des composants OpenSSH modifiés (ShieldSlide) pour recueillir des informations d'identification et obtenir un accès persistant.

**Vulnérabilités Exploités (avec CVE si possible) :**

*   Citrix NetScaler ADC et NetScaler Gateway : CVE-2023-3519
*   Commvault : CVE-2025-3928
*   Vulnérabilités zero-day sur Microsoft Exchange Server (mentionné historiquement)
*   CVE-2016-5195 (Dirty COW)
*   CVE-2021-4034 (PwnKit)

**Recommandations :**

Bien que l'article ne fournisse pas explicitement une section de recommandations, les tactiques décrites impliquent les actions suivantes pour atténuer les risques :

*   **Sécuriser les appliances exposées sur Internet** : Appliquer les correctifs de sécurité rapidement pour les dispositifs et applications accessibles depuis Internet.
*   **Renforcer les relations de confiance dans le cloud** : Mettre en place des contrôles d'accès stricts et auditer régulièrement les permissions accordées aux partenaires et aux fournisseurs de services cloud.
*   **Surveillance de l'activité cloud** : Monitorer l'accès aux ressources cloud, les requêtes à l'Instance Metadata Service (IMDS) et les modifications des configurations du plan de contrôle.
*   **Gestion des vulnérabilités** : Mettre en place un programme robuste de gestion des vulnérabilités pour identifier et corriger rapidement les failles, y compris celles des anciens systèmes d'exploitation.
*   **Sécurisation des accès** : Utiliser l'authentification multifacteur et mettre en œuvre des politiques de mots de passe forts.
*   **Protection des systèmes Linux** : Assurer la sécurité des environnements Linux utilisés dans le secteur des télécommunications, y compris les mises à jour et la surveillance des processus.
*   **Détection et réponse aux menaces** : Mettre en place des outils et des processus pour détecter les comportements suspects tels que l'utilisation de web shells, de malware RAT et les modifications de fichiers binaires légitimes comme OpenSSH.

---
[Source](https://thehackernews.com/2025/08/chinese-hackers-murky-genesis-and.html){:target="_blank"}
