---
title: 'Deep dive into DragonForce ransomware and its Scattered Spider connection'
date: 2025-12-03
permalink: /posts/2025/12/03/deep-dive-into-dragonforce-ransomware-and-its-scattered-spider-connection/
tags:
- veille-cyber
- bleepingcomp
---
**DragonForce : La nouvelle menace des cartels du ransomware**

DragonForce, un groupe de ransomware apparu en 2023, s'est réorganisé en un "cartel du ransomware", élargissant ses opérations à l'échelle mondiale. Il collabore notamment avec le groupe Scattered Spider, connu pour ses techniques avancées d'ingénierie sociale et d'obtention d'accès initiaux.

Cette alliance permet à DragonForce d'exploiter des vulnérabilités dans les pilotes de sécurité (tels que truesight.sys et rentdrv2.sys) pour désactiver les protections et contourner les failles d'encryptage précédemment associées au ransomware Akira.

**Points clés :**

*   **Modèle "Ransomware-as-a-Service" (RaaS) amélioré :** DragonForce recrute des cybercriminels en leur proposant 80% des profits, des encryptors personnalisables et une infrastructure.
*   **Synergie avec Scattered Spider :** Ce dernier utilise l'ingénierie sociale pour obtenir des identifiants, contourner l'authentification multifacteur (MFA) par des méthodes comme la fatigue MFA ou le SIM swapping, et établir une persistance dans le réseau via des outils RMM.
*   **Exfiltration et chiffrement :** Les données sont exfiltrées vers des services cloud (MEGA, Amazon S3) avant le chiffrement des systèmes Windows, Linux et ESXi.
*   **Évolution stratégique :** Le passage à un modèle de "cartel" favorise la flexibilité opérationnelle et la coopération entre acteurs malveillants spécialisés, rendant la défense plus complexe.

**Vulnérabilités exploitées :**

*   Exploitation de pilotes système vulnérables (ex: truesight.sys, rentdrv2.sys) pour désactiver les mesures de sécurité.
*   Exploitation de vulnérabilités d'encryptage précédemment liées au ransomware Akira.
*   Utilisation de techniques d'ingénierie sociale avancées pour contourner l'authentification multifacteur (MFA).

**Recommandations :**

*   **MFA résistante au phishing :** Implémenter et appliquer strictement des méthodes d'authentification multifacteur qui ne peuvent pas être contournées par des attaques de phishing.
*   **Solutions EDR robustes :** Déployer des systèmes de détection et de réponse d'endpoints (EDR) capables d'alerter sur le déploiement d'outils de surveillance à distance et l'utilisation de pilotes système suspects.
*   **Anticipation des attaques collaboratives :** Comprendre que les menaces actuelles sont souvent des intrusions coordonnées impliquant plusieurs entités spécialisées, et adapter les stratégies de défense en conséquence.

---
[Source](https://www.bleepingcomputer.com/news/security/deep-dive-into-dragonforce-ransomware-and-its-scattered-spider-connection/){:target="_blank"}
