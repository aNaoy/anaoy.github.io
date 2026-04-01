---
title: 'Casbaneiro Phishing Targets Latin America and Europe Using Dynamic PDF Lures'
date: 2026-04-01
permalink: /posts/2026/04/01/casbaneiro-phishing-targets-latin-america-and-europe-using-dynamic-pdf-lures/
tags:
- veille-cyber
- hackernews
---
### Campagne de phishing Casbaneiro : Propagation automatisée via PDF dynamiques

Un groupe cybercriminel brésilien, identifié sous les noms « Augmented Marauder » et « Water Saci », mène actuellement une campagne de phishing sophistiquée ciblant des entreprises en Amérique latine et en Europe. Cette offensive combine l'utilisation du cheval de Troie bancaire **Casbaneiro** et du malware de propagation **Horabot**.

**Points clés :**
* **Vecteur d'attaque :** Utilisation de courriels usurpant des convocations judiciaires contenant des PDF protégés par mot de passe.
* **Mécanisme dynamique :** Le malware utilise une API PHP pour générer à la volée des PDF personnalisés afin de tromper les cibles.
* **Propagation auto-entretenue :** Une fois infecté, le système utilise les contacts Microsoft Outlook de la victime pour diffuser automatiquement le phishing à d'autres cibles, transformant les postes compromis en nœuds de propagation.
* **Multi-canal :** En plus des emails, les attaquants utilisent WhatsApp et la technique de « ClickFix » (invitant l'utilisateur à exécuter des fichiers HTA malveillants sous couvert de correction de problème technique).
* **Techniques avancées :** Utilisation de scripts VBS pour l'anti-analyse et détection de solutions de sécurité (ex: Avast).

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée, l'attaque repose sur l'ingénierie sociale (convocation judiciaire), l'exécution de scripts (HTA, VBS, PowerShell) et l'abus de fonctionnalités légitimes (Outlook, API PHP, AutoIt).

**Recommandations :**
* **Sensibilisation :** Former les utilisateurs aux risques liés aux pièces jointes inattendues, même si elles semblent provenir de contacts connus ou d'autorités judiciaires.
* **Filtrage des emails :** Renforcer les politiques de filtrage pour bloquer les fichiers compressés (ZIP) contenant des scripts ou des fichiers exécutables (HTA, VBS, .at, .ia).
* **Surveillance EDR :** Détecter les comportements suspects tels que l'exécution de scripts PowerShell non autorisés, l'utilisation inhabituelle de l'API Outlook ou des activités anormales liées au processus AutoIt.
* **Contrôle d'accès :** Restreindre l'exécution de scripts sur les postes de travail et limiter les privilèges des utilisateurs pour empêcher l'installation de payloads secondaires.

---
[Source](https://thehackernews.com/2026/04/casbaneiro-phishing-targets-latin.html){:target="_blank"}
