---
title: 'Reynolds Ransomware Embeds BYOVD Driver to Disable EDR Security Tools'
date: 2026-02-10
permalink: /posts/2026/02/10/reynolds-ransomware-embeds-byovd-driver-to-disable-edr-security-tools/
tags:
- veille-cyber
- hackernews
---
## Reynolds Ransomware : Une Nouvelle Menace Intègre des Pilotes Vulnérables pour Désactiver les Défenses

Une nouvelle famille de rançongiciels, baptisée **Reynolds**, se distingue par sa capacité à intégrer directement dans sa charge utile un composant "Bring Your Own Vulnerable Driver" (BYOVD). Cette technique vise à exploiter des pilotes légitimes mais vulnérables pour obtenir des privilèges élevés et neutraliser les solutions de détection et réponse des points d'extrémité (EDR), permettant ainsi aux activités malveillantes de passer inaperçues.

Contrairement aux méthodes traditionnelles où un outil distinct est déployé avant le rançongiciel pour désactiver les logiciels de sécurité, Reynolds embarque directement le pilote NsecSoft NSecKrnl. Ce pilote est connu pour être affecté par une faille de sécurité (CVE-2025-68947) qui peut être exploitée pour terminer des processus arbitraires.

L'objectif de cette intégration est double : rendre plus difficile l'intervention des défenseurs en regroupant les capacités d'évasion et de rançongiciel, et simplifier le processus pour les affiliés en évitant de déployer des fichiers externes séparément. Le rançongiciel Reynolds est conçu pour désactiver les processus associés à divers programmes de sécurité tels qu'Avast, CrowdStrike Falcon, Palo Alto Networks Cortex XDR, Sophos et Symantec Endpoint Protection.

La présence d'un chargeur suspect, chargé latéralement, a été observée sur le réseau des cibles plusieurs semaines avant le déploiement du rançongiciel. De plus, l'outil d'accès à distance GotoHTTP a été déployé après l'attaque, suggérant une intention de maintenir un accès persistant aux systèmes compromis.

**Points Clés :**

*   **Intégration du BYOVD :** Le rançongiciel Reynolds intègre un pilote vulnérable directement dans sa charge utile pour désactiver les outils de sécurité.
*   **Ciblage des EDR :** La technique BYOVD vise spécifiquement à contourner les solutions de détection et réponse des points d'extrémité.
*   **Simplification pour les attaquants :** L'intégration du composant d'évasion réduit la complexité des opérations pour les acteurs malveillants.
*   **Accès persistant :** L'utilisation d'outils comme GotoHTTP suggère une volonté de maintenir la présence sur les systèmes compromis.

**Vulnérabilités :**

*   **CVE-2025-68947 :** Faille dans le pilote NsecSoft NSecKrnl permettant la terminaison de processus arbitraires.

**Recommandations :**

*   Bien que l'article ne fournisse pas de recommandations directes, les pratiques générales de cybersécurité s'appliquent, notamment le maintien à jour des logiciels, l'utilisation de solutions de sécurité robustes et la surveillance des réseaux pour détecter les activités suspectes. Il est crucial de surveiller l'évolution des techniques d'évasion utilisées par les rançongiciels comme Reynolds.

---
[Source](https://thehackernews.com/2026/02/reynolds-ransomware-embeds-byovd-driver.html){:target="_blank"}
