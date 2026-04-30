---
title: 'Danger of Libredtail &#x5b;Guest Diary&#x5d;, (Wed, Apr 29th)'
date: 2026-04-30
permalink: /posts/2026/04/30/danger-of-libredtail-x5bguest-diaryx5d-wed-apr-29th/
tags:
- veille-cyber
- sans-isc
---
### Analyse de la menace : Le malware de cryptominage Redtail

Cette étude, menée via le réseau de honeypots DShield, met en lumière une campagne active exploitant des vulnérabilités PHP pour déployer le malware de cryptominage « Redtail ». Les attaquants utilisent des requêtes HTTP POST pour automatiser l'exécution de scripts malveillants sur les serveurs ciblés.

**Points clés :**
*   **Mode opératoire :** Les attaquants utilisent des scans de ports et des tentatives d'accès SSH (souvent via le couple admin/admin), couplés à des attaques HTTP automatisées.
*   **Techniques d'obfuscation :** Les requêtes sont encodées en Base64 et utilisent des traversées de répertoire pour identifier des configurations CGI vulnérables.
*   **Objectif :** Téléchargement et exécution de scripts de persistance (`apache.selfrep`, `cve_2024_4577.selfrep`) visant à supprimer les mineurs concurrents et à installer une version adaptée de Redtail selon l'architecture du système (x86_64, ARM, etc.).

**Vulnérabilité exploitée :**
*   **CVE-2024-4577 :** Une vulnérabilité critique dans PHP (CGI) qui permet l'exécution de code arbitraire en raison d'une mauvaise gestion des caractères (comportement « Best-Fit »), facilitant ainsi l'injection de commandes via des paramètres PHP malveillants.

**Recommandations de protection :**
*   **Mise à jour :** Appliquer les correctifs de sécurité pour PHP afin de corriger la faille CVE-2024-4577.
*   **Filtrage réseau :** Bloquer le User-Agent associé à cette campagne sur vos WAF, reverse proxies ou IPS.
*   **Durcissement :** Restreindre les accès SSH en utilisant exclusivement des clés d'authentification plutôt que des mots de passe.
*   **Surveillance :** Surveiller les flux HTTP pour détecter des tentatives d'accès inhabituelles vers `/sh` ou des exécutions suspectes de `wget`/`curl` suivies de `sh`.
*   **Firewall :** Bloquer les connexions sortantes vers les adresses IP identifiées comme infrastructure de distribution de payloads (ex: `31.57.216.121`, `178.16.55.224`, `46.151.182.82`).

---
[Source](https://isc.sans.edu/diary/rss/32936){:target="_blank"}
