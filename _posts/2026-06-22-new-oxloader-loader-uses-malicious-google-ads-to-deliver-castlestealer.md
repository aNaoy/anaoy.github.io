---
title: 'New OXLOADER Loader Uses Malicious Google Ads to Deliver CastleStealer'
date: 2026-06-22
permalink: /posts/2026/06/22/new-oxloader-loader-uses-malicious-google-ads-to-deliver-castlestealer/
tags:
- veille-cyber
- hackernews
---
### Campagne malveillante : Le chargeur OXLOADER diffuse CastleStealer via Google Ads

Une nouvelle campagne, identifiée sous le nom de code **REF8372**, utilise le chargeur de logiciels malveillants **OXLOADER** pour infecter les utilisateurs avec le voleur d'informations **CastleStealer**. Les auteurs, probablement russophones et motivés par le gain financier, ciblent les utilisateurs cherchant des logiciels populaires via des publicités Google détournées.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation de publicités Google trompeuses redirigeant vers des sites frauduleux (ex: usurpation de Node.js).
*   **Abus de services légitimes :** Le malware utilise la plateforme de stockage décentralisée **Storj** pour héberger ses scripts et exécutables, contournant ainsi les filtres de réputation de domaines.
*   **Techniques d'évasion :** OXLOADER intègre des mesures sophistiquées : obfuscation poussée (*Control-Flow Flattening*, *Mixed Boolean-Arithmetic*), détection d'environnements virtualisés (anti-VM) et utilisation du détournement de DLL (*DLL side-loading*).
*   **Ciblage :** Le logiciel malveillant contient des exclusions empêchant l'infection des systèmes situés dans la région de la CEI (Communauté des États indépendants).
*   **Composant final :** Une fois actif, le chargeur déchiffre et exécute **CastleStealer**, un malware .NET conçu pour exfiltrer des données sensibles.

**Vulnérabilités :**
*   Il ne s'agit pas de vulnérabilités logicielles spécifiques (CVE), mais de l'exploitation de mécanismes Windows légitimes, notamment le **UAC (User Account Control)** via l'élévation de privilèges (`-Verb RunAs`) et le détournement de **DLL**.

**Recommandations :**
*   **Vigilance publicitaire :** Faire preuve d'une extrême prudence lors du clic sur les liens sponsorisés dans les moteurs de recherche ; vérifier systématiquement l'URL de destination.
*   **Sécurité des terminaux :** Utiliser des solutions EDR/XDR capables de détecter les comportements suspects (ex: exécution de PowerShell inhabituelle, élévation de privilèges non sollicitée, ou activités suspectes liées au chargement de DLL).
*   **Filtrage réseau :** Surveiller les flux vers les plateformes de stockage cloud décentralisées si celles-ci ne sont pas nécessaires à l'activité métier.
*   **Politique de moindre privilège :** Restreindre les droits d'administration locale pour limiter l'impact des techniques d'élévation de privilèges (UAC).

---
[Source](https://thehackernews.com/2026/06/new-oxloader-loader-uses-malicious.html){:target="_blank"}
