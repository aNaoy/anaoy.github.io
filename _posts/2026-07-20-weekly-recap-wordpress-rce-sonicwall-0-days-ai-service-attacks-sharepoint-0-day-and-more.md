---
title: '⚡ Weekly Recap: WordPress RCE, SonicWall 0-Days, AI Service Attacks, SharePoint 0-Day and More'
date: 2026-07-20
permalink: /posts/2026/07/20/weekly-recap-wordpress-rce-sonicwall-0-days-ai-service-attacks-sharepoint-0-day-and-more/
tags:
- veille-cyber
- hackernews
---
### Actualités Cybersécurité : Vulnérabilités Critiques et Menaces Émergentes

Cette semaine a été marquée par une vague d'exploitations de vulnérabilités "0-day" et l'émergence de campagnes sophistiquées, souvent facilitées par des outils assistés par IA.

#### Points Clés
*   **WordPress :** Une faille critique dans le cœur de WordPress permet une exécution de code à distance (RCE) sans authentification.
*   **SonicWall :** Des attaquants (UTA0533) ont exploité des vulnérabilités 0-day sur des VPN SMA 1000 avant leur divulgation publique.
*   **Microsoft :** Une faille RCE critique dans SharePoint a été ajoutée au catalogue KEV de la CISA suite à des exploitations actives.
*   **Botnets IA :** Le botnet NadMesh cible activement les services d'IA exposés (Ollama, ComfyUI, etc.) pour dérober des jetons Kubernetes et des clés AWS.
*   **Malwares :** Le framework OkoBot infecte Windows pour voler des phrases de récupération de portefeuilles crypto via des extensions de navigateur malveillantes.
*   **Défense :** Le ransomware Qilin utilise des "EDR killers" basés sur des pilotes vulnérables pour désactiver les solutions de sécurité au niveau du noyau.

#### Vulnérabilités Majeures
*   **WordPress Core :** CVE-2026-63030 et CVE-2026-60137 (Chaînage pour RCE).
*   **SonicWall SMA :** CVE-2026-15409 (Score CVSS 10.0) et CVE-2026-15410 (Score CVSS 7.2) pour exécution de commandes.
*   **Microsoft SharePoint :** CVE-2026-58644 (RCE, Score CVSS 9.8).
*   **OpenSSL (HollowByte) :** Faille DoS permettant l'épuisement de la mémoire vive par une charge utile de 11 octets.

#### Recommandations
1.  **Prioriser les correctifs :** Appliquer immédiatement les patchs pour WordPress, SharePoint, SonicWall et OpenSSL.
2.  **Audit de sécurité :** Vérifier les systèmes exposés (notamment les services d'IA et les interfaces de gestion) pour détecter des signes de compromission (backdoors SSH, fichiers suspects dans `/tmp` ou `/var/tmp`).
3.  **Gestion des accès :** Appliquer le principe du moindre privilège, particulièrement pour les agents IA et les serveurs d'orchestration.
4.  **Détection :** Surveiller l'exécution de pilotes suspects ou non signés, souvent utilisés par les ransomwares pour contourner les protections EDR.
5.  **Revue de code :** Pour les environnements de développement, envisager l'utilisation d'outils d'audit automatisés tout en maintenant une vigilance humaine face à la vitesse de production de code assisté par IA.

---
[Source](https://thehackernews.com/2026/07/weekly-recap-wordpress-rce-sonicwall-0.html){:target="_blank"}
