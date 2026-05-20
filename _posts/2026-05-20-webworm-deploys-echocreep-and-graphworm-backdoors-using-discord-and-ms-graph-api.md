---
title: 'Webworm Deploys EchoCreep and GraphWorm Backdoors Using Discord and MS Graph API'
date: 2026-05-20
permalink: /posts/2026/05/20/webworm-deploys-echocreep-and-graphworm-backdoors-using-discord-and-ms-graph-api/
tags:
- veille-cyber
- hackernews
---
### Webworm : Nouvelles techniques de dissimulation et backdoors via Discord et Microsoft Graph

Le groupe cybercriminel chinois **Webworm** a fait évoluer son arsenal en 2025, délaissant les chevaux de Troie d'accès à distance (RAT) classiques au profit d'outils de proxy furtifs et de deux nouvelles backdoors : **EchoCreep** (utilisant Discord pour le contrôle) et **GraphWorm** (exploitant l'API Microsoft Graph et OneDrive). Le groupe cible désormais les gouvernements et entreprises en Europe, Afrique du Sud et Asie, en utilisant le VPN SoftEther et des dépôts GitHub factices pour masquer ses activités.

**Points clés :**
*   **Évolution tactique :** Passage des RAT (Trochilus, 9002, Gh0st) vers des outils de proxy personnalisés (WormFrp, ChainWorm, etc.) capables de chaînage réseau pour une meilleure furtivité.
*   **Canaux de C2 :** Utilisation détournée de services légitimes pour éviter la détection réseau.
*   **Reconnaissance :** Emploi d'outils open-source tels que `dirsearch` et `nuclei` pour le scan de vulnérabilités et l'énumération de répertoires sur les serveurs web ciblés.
*   **MaaS (Malware-as-a-Service) :** Le groupe interagit dans un écosystème plus large incluant le malware **BadIIS**, utilisé par plusieurs acteurs chinois pour le détournement de trafic SEO et le proxying inverse sur les serveurs IIS.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, mais le groupe exploite activement les vulnérabilités non corrigées sur les serveurs web (via *brute-force* et scan automatisé) ainsi que les mauvaises configurations d'accès.

**Recommandations :**
*   **Surveillance réseau :** Bloquer ou inspecter rigoureusement les flux sortants vers les API Discord et Microsoft Graph depuis les serveurs sensibles.
*   **Sécurisation IIS :** Mettre à jour et auditer régulièrement les serveurs IIS pour détecter la présence de modules malveillants ou de comportements suspects liés à BadIIS.
*   **Gestion des accès :** Appliquer le principe du moindre privilège, particulièrement pour les applications connectées à l'API Microsoft Graph (OneDrive).
*   **Détection d'outils :** Surveiller l'utilisation suspecte d'outils de scan web (`dirsearch`, `nuclei`) et la présence de clients VPN comme SoftEther non autorisés sur le parc informatique.

---
[Source](https://thehackernews.com/2026/05/webworm-deploys-echocreep-and-graphworm.html){:target="_blank"}
