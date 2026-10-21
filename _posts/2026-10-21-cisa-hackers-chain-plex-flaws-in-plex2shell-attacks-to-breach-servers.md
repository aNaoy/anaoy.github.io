---
title: 'CISA: Hackers chain Plex flaws in Plex2Shell attacks to breach servers'
date: 2026-10-21
permalink: /posts/2026/10/21/cisa-hackers-chain-plex-flaws-in-plex2shell-attacks-to-breach-servers/
tags:
- veille-cyber
- bleepingcomp
---
### Menaces actives : exploitation de vulnérabilités critiques dans Plex et autres logiciels

La CISA a émis une alerte concernant une campagne d'attaques active nommée **Plex2Shell**, ciblant les serveurs Plex Media Server. En enchaînant quatre vulnérabilités, des attaquants peuvent obtenir des jetons d'administration et exécuter du code à distance avec des privilèges élevés. Des activités malveillantes, incluant le déploiement de cryptomineurs, ont déjà été observées.

**Points clés :**
*   La chaîne d'exploitation "Plex2Shell" est jugée critique (score CVSS de 9.8).
*   Des vulnérabilités supplémentaires dans **Siemens Software Center** (CVE-2026-110936) et **SiteGuard Server Edition** (CVE-2026-106931) sont également activement exploitées et ajoutées au catalogue KEV de la CISA.

**Vulnérabilités Plex (Plex2Shell) :**
*   **CVE-2026-96652 :** SSRF dans `/player/timeline` permettant des requêtes non authentifiées.
*   **CVE-2026-96654 :** Injection d'URL dans `searchOne` permettant l'invocation de fonctions de plugins.
*   **CVE-2026-96655 :** SSRF authentifié dans le point de terminaison du transcodeur.
*   **CVE-2026-96656 :** Écriture arbitraire de fichiers permettant l'exécution de code via des bibliothèques partagées malveillantes.

**Recommandations :**
*   **Plex Media Server :** Mettre à jour immédiatement vers une version égale ou supérieure à **1.43.3.10861**.
*   **Siemens Software Center :** Mettre à jour vers la version **4.0.9.8** ou ultérieure.
*   **SiteGuard Server Edition :** Appliquer les mises à jour vers la version **8.00 Update 5** ou **7.00 Update 6** selon l'environnement.
*   Les administrateurs fédéraux et les organisations doivent prioriser ces correctifs pour contrer les campagnes d'exploitation en cours.

---
[Source](https://www.bleepingcomputer.com/news/security/cisa-hackers-chain-plex-flaws-in-plex2shell-attacks-to-breach-servers/){:target="_blank"}
