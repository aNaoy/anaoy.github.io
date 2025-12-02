---
title: '&#x5b;Guest Diary&#x5d; Hunting for SharePoint In-Memory ToolShell Payloads, (Tue, Dec 2nd)'
date: 2025-12-02
permalink: /posts/2025/12/02/x5bguest-diaryx5d-hunting-for-sharepoint-in-memory-toolshell-payloads-tue-dec-2nd/
tags:
- veille-cyber
- sans-isc
---
**Détection et Analyse des Exploits In-Memory ToolShell sur SharePoint**

Une technique d'exploitation avancée, surnommée ToolShell, cible les versions sur site de Microsoft SharePoint Server 2016, 2019 et les éditions par abonnement. Initialement, les attaquants utilisaient des charges utiles permettant d'injecter des web shells dans le système de fichiers, facilement détectables. Pour contourner les solutions de sécurité (EDR), les attaquants ont évolué vers des charges utiles exécutées directement en mémoire, rendant leur détection plus complexe.

**Points Clés :**

*   **Exploitation en mémoire :** Les acteurs malveillants privilégient désormais les charges utiles s'exécutant en mémoire pour échapper aux détections traditionnelles basées sur les fichiers.
*   **Outils de chasse :** L'article présente une méthodologie de détection et d'analyse utilisant Zeek Network Security Monitor, DaemonLogger et Wireshark.
*   **Indicateurs de compromission :** Des schémas d'URL spécifiques (`/_layouts/15/ToolPane.aspx/` ou `/_layouts/16/ToolPane.aspx/`), des en-têtes "Referer" (`/_layouts/SignOut.aspx`) et des requêtes POST avec un corps de requête non vide sont identifiés comme des indicateurs potentiels d'exploitation.
*   **Analyse des charges utiles :** Le processus décrit permet de décoder les données encodées et compressées au sein des requêtes HTTP pour révéler les charges utiles malveillantes, notamment des bibliothèques .NET (DLL) et des commandes PowerShell encodées.

**Vulnérabilités :**

*   **CVE-2025-53770 :** Vulnérabilité de désérialisation dans SharePoint Server.
*   **CVE-2025-53771 :** Vulnérabilité de contournement d'authentification dans SharePoint Server.

**Recommandations :**

*   Surveiller activement les journaux Zeek pour détecter les requêtes HTTP correspondant aux indicateurs mentionnés.
*   Utiliser des outils comme DaemonLogger pour capturer le trafic réseau et Wireshark pour l'analyse détaillée des paquets.
*   Développer et appliquer des processus pour décoder et analyser les charges utiles en mémoire afin d'identifier les activités malveillantes.
*   Être vigilant face aux nouvelles techniques d'exécution en mémoire utilisées par les attaquants.
*   Appliquer les correctifs de sécurité disponibles pour les vulnérabilités CVE-2025-53770 et CVE-2025-53771.

---
[Source](https://isc.sans.edu/diary/rss/32524){:target="_blank"}
