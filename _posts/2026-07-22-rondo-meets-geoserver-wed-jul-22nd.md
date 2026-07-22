---
title: 'Rondo Meets Geoserver, (Wed, Jul 22nd)'
date: 2026-07-22
permalink: /posts/2026/07/22/rondo-meets-geoserver-wed-jul-22nd/
tags:
- veille-cyber
- sans-isc
---
### Recrudescence des attaques du botnet Rondo visant GeoServer

Une campagne d'attaques exploitant une vulnérabilité critique dans GeoServer, un logiciel de gestion de données géographiques, a été observée. Les attaquants utilisent des requêtes malveillantes pour injecter du code arbitraire visant à déployer le botnet « Rondo ».

**Points clés :**
*   **Vecteur d'attaque :** Utilisation de requêtes WFS (Web Feature Service) spécialement formées pour exploiter une faille d'injection.
*   **Méthodologie :** Le code malveillant est dissimulé via un encodage URL puis Base64. Une fois exécuté, le script tente de télécharger et d'exécuter un payload (fichier `rondo.zyt.sh`) depuis un serveur distant via `wget` ou `curl`.
*   **Historique :** Ce botnet est connu pour cibler spécifiquement les instances GeoServer vulnérables, employant parfois des références à des rappeurs dans son code.

**Vulnérabilité identifiée :**
*   **CVE-2024-36401 :** Problème d'évaluation d'expressions X-Path dans GeoServer permettant l'exécution de code à distance (RCE).

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs de sécurité fournis par l'éditeur de GeoServer pour neutraliser la vulnérabilité CVE-2024-36401.
*   **Monitoring :** Surveiller les journaux d'accès (logs) pour détecter des requêtes suspectes contenant des appels `java.lang.Runtime.getRuntime()` ou des tentatives de téléchargement de scripts Shell (`.sh`).
*   **Filtrage :** Bloquer les communications sortantes vers des adresses IP suspectes connues pour héberger des payloads de botnets.

---
[Source](https://isc.sans.edu/diary/rss/33176){:target="_blank"}
