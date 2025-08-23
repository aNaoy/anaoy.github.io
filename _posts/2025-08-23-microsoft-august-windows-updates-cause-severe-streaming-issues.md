---
title: 'Microsoft: August Windows updates cause severe streaming issues'
date: 2025-08-23
permalink: /posts/2025/08/23/microsoft-august-windows-updates-cause-severe-streaming-issues/
tags:
- veille-cyber
- bleepingcomp
---
**Mises à jour Windows d'août : Problèmes de performance avec NDI**

Les mises à jour de sécurité Windows d'août 2025 causent d'importants ralentissements et saccades lors de l'utilisation de logiciels de streaming NDI sur certaines configurations Windows 10 et Windows 11. Ces problèmes affectent des applications comme OBS (Open Broadcast Software) et NDI Tools, particulièrement lorsque la "Capture d'écran" est activée sur le PC source, et ce, même avec une faible bande passante.

Ces dysfonctionnements sont apparus suite à l'installation des mises à jour KB5063878 pour Windows 11 24H2 et KB5063709 pour Windows 10 21H2/22H2. Le protocole RUDP utilisé par NDI est spécifiquement impacté, provoquant des interruptions de trafic inattendues, tandis que les connexions UDP ou TCP simple ne sont pas affectées.

Microsoft reconnaît ces problèmes et travaille à leur résolution. En attendant, une solution temporaire proposée par NDI consiste à modifier le mode de réception NDI pour utiliser TCP ou UDP à la place de RUDP. Cela s'effectue via l'application NDI Access Manager, dans l'onglet "Avancé".

Il est à noter que ces mêmes mises à jour d'août ont également engendré d'autres soucis, tels que des erreurs lors de l'installation via WSUS (corrigées par la suite) et des problèmes avec les fonctions de réinitialisation et de récupération de Windows, ayant nécessité des mises à jour d'urgence. Microsoft sollicite également des retours d'information concernant des défaillances et des corruptions de données sur les SSD et HDD suite à l'installation de ces mises à jour.

**Points Clés :**

*   **Problème :** Ralentissements et saccades avec les logiciels de streaming NDI.
*   **Cause :** Mises à jour de sécurité Windows d'août 2025 (KB5063878, KB5063709).
*   **Logiciels affectés :** OBS, NDI Tools, etc.
*   **Protocole impacté :** NDI utilisant RUDP.
*   **Systèmes concernés :** Windows 10 (21H2/22H2) et Windows 11 (24H2).

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans cet article, mais plutôt un dysfonctionnement introduit par les mises à jour.

**Recommandations :**

*   **Solution Temporaire :** Modifier le mode de réception NDI pour utiliser TCP ou UDP via NDI Access Manager (onglet Avancé).
*   **Attente :** La résolution définitive du problème par Microsoft est en cours.
*   **Surveillance :** Être attentif aux autres problèmes potentiels liés à ces mises à jour et suivre les communications de Microsoft.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-august-windows-updates-cause-severe-ndi-streaming-issues/){:target="_blank"}
