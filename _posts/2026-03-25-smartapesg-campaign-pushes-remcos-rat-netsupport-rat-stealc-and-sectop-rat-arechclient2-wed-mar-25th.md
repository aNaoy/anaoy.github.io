---
title: 'SmartApeSG campaign pushes Remcos RAT, NetSupport RAT, StealC, and Sectop RAT (ArechClient2), (Wed, Mar 25th)'
date: 2026-03-25
permalink: /posts/2026/03/25/smartapesg-campaign-pushes-remcos-rat-netsupport-rat-stealc-and-sectop-rat-arechclient2-wed-mar-25th/
tags:
- veille-cyber
- sans-isc
---
### Analyse de la campagne malveillante SmartApeSG

La campagne **SmartApeSG** exploite la technique d'ingénierie sociale dite **« ClickFix »**, qui consiste à inciter les utilisateurs à copier-coller un script malveillant via un faux CAPTCHA sur des sites web compromis. Une fois exécutée, cette procédure ouvre la porte à une série d'infections successives.

**Points clés :**
*   **Mode opératoire :** L'attaque commence par une injection JavaScript sur des sites légitimes, suivie d'une redirection vers une page de faux CAPTCHA demandant une interaction utilisateur.
*   **Chaîne d'infection :** L'infection initiale par **Remcos RAT** sert de vecteur pour télécharger et installer d'autres charges utiles de manière différée (jusqu'à plus de deux heures après l'intrusion initiale).
*   **Malwares déployés :** La campagne installe successivement Remcos RAT, NetSupport RAT, StealC et Sectop RAT (ArechClient2).
*   **Techniques utilisées :** Utilisation intensive du **DLL side-loading** (chargement de DLL malveillantes via des exécutables légitimes) pour dissimuler les activités.

**Vulnérabilités :**
*   L'attaque n'exploite pas une faille logicielle spécifique (CVE), mais abuse de la confiance des utilisateurs et de l'exécution de scripts locaux (fichiers HTA et archives compressées) pour compromettre le système.

**Indicateurs de compromission (IoC) :**
*   **Domaines :** `fresicrto[.]top`, `urotypos[.]com`.
*   **Serveurs C2 :** 
    *   Remcos RAT : `95.142.45[.]231:443`
    *   NetSupport RAT : `185.163.47[.]220:443`
    *   StealC : `89.46.38[.]100:80`
    *   Sectop RAT : `195.85.115[.]11:9000`

**Recommandations :**
*   **Sensibilisation :** Éduquer les utilisateurs sur les dangers des invites « copier-coller » provenant de pages web suspectes, même sur des sites familiers.
*   **Filtrage réseau :** Bloquer les connexions sortantes vers des domaines et adresses IP non identifiés, particulièrement si elles sont associées à des ports de communication inhabituels.
*   **Sécurité des terminaux :** Restreindre l'exécution de fichiers HTA et surveiller le comportement des processus suspects qui tentent de charger des DLL dans des dossiers système (`C:\ProgramData` ou `AppData`).
*   **Mise à jour :** Maintenir les solutions EDR/Antivirus à jour pour détecter les signatures des malwares mentionnés et leurs mécanismes de side-loading.

---
[Source](https://isc.sans.edu/diary/rss/32826){:target="_blank"}
