---
title: 'Russian APT28 Breaches NATO Naval Shipbuilder in NATO Country, Deploys New Reflective Loader'
date: 2026-10-20
permalink: /posts/2026/10/20/russian-apt28-breaches-nato-naval-shipbuilder-in-nato-country-deploys-new-reflective-loader/
tags:
- veille-cyber
- hackernews
---
### Offensive cyber-opérations russes contre l'OTAN et l'Ukraine

Le groupe APT28 (Fancy Bear) intensifie ses activités d'espionnage contre des entités stratégiques de l'OTAN, notamment dans les secteurs naval et aéronautique militaire. Parallèlement, les acteurs étatiques russes ciblent massivement l'Ukraine via des attaques mobiles sophistiquées et l'exploitation de vulnérabilités logicielles.

**Points clés :**
*   **Infiltration de l'OTAN :** Utilisation du backdoor « HOOKEDGE » (évolutif vers des communications IP directes plutôt que via des services web tiers) et d'un nouveau chargeur (loader) réflexif nommé `ld.exe`.
*   **Techniques d'accès :** Persistance via des tunnels SSH, vol d'identifiants (via SSH ou capture de hash NTLM PowerShell) et exécution de commandes en mémoire.
*   **Espionnage mobile en Ukraine :** Recours aux kits d'exploitation iOS (DarkSword, Coruna) pour le vol de données sur les appareils de responsables militaires et gouvernementaux.
*   **Malwares Android :** Utilisation de logiciels malveillants comme CAMELSPY et BTMOB RAT pour l'exfiltration de données personnelles et professionnelles.

**Vulnérabilités exploitées :**
*   **CVE-2026-21509 :** Contournement de fonctionnalité de sécurité dans Microsoft Office.
*   **CVE-2026-8496 :** Vulnérabilité "zero-click" dans le client webmail SOGo.
*   **Autres :** Failles XSS persistantes dans le client webmail Roundcube.

**Recommandations :**
*   **Surveillance réseau :** Bloquer les communications vers les adresses IP suspectes identifiées (notamment `185.82.218[.]119` et les serveurs C2 de type LegionRelay).
*   **Gestion des accès :** Restreindre l'usage de SSH et des scripts PowerShell non autorisés ; auditer régulièrement les sessions persistantes sur les serveurs critiques.
*   **Sécurisation des terminaux :** Appliquer les correctifs pour les failles Office et webmail ; maintenir les systèmes d'exploitation mobiles à jour et limiter l'utilisation d'applications tierces non vérifiées pour le personnel sensible.
*   **Contrôle des documents :** Désactiver les macros dans les documents Office (Word/Excel) pour prévenir l'exécution de scripts malveillants de type HOOKEDGE.

---
[Source](https://thehackernews.com/2026/10/russian-apt28-breaches-nato-naval.html){:target="_blank"}
