---
title: 'Fake Claude Code install guides push infostealers in InstallFix attacks'
date: 2026-03-06
permalink: /posts/2026/03/06/fake-claude-code-install-guides-push-infostealers-in-installfix-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Menace InstallFix : Des guides d'installation factices pour voler vos données

Des cybercriminels exploitent une variante de l'ingénierie sociale appelée « InstallFix » pour propager des logiciels malveillants. En utilisant des publicités malveillantes (malvertising) sur Google, les attaquants dirigent les utilisateurs vers des sites clonés, reproduisant fidèlement la documentation officielle d'outils populaires comme Claude Code. L'objectif est d'inciter les développeurs à copier-coller des commandes d'installation malveillantes dans leur terminal.

**Points clés :**
* **Technique :** Les attaquants clonent des pages de documentation légitimes et insèrent des commandes `curl-to-bash` (macOS) ou des scripts PowerShell/CMD (Windows) malveillants.
* **Leurre :** Une fois la commande exécutée, le site redirige vers le vrai service (ex: Anthropic), laissant la victime croire que tout a fonctionné normalement.
* **Infection :** Le logiciel malveillant déployé est le **Amatera Stealer**, un infostealer capable de dérober des portefeuilles de cryptomonnaies, des identifiants, des cookies et des jetons de session.
* **Persistance :** Les sites frauduleux sont hébergés sur des plateformes légitimes comme Squarespace ou Cloudflare, ce qui renforce leur crédibilité.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée, car il s'agit d'une exploitation de l'ingénierie sociale et d'une confiance excessive envers les commandes `curl-to-bash` copiées depuis des sources web non vérifiées.

**Recommandations :**
* **Vérification :** Obtenez toujours vos instructions d'installation exclusivement sur les dépôts officiels (GitHub, sites web de l'éditeur) en accédant directement à l'URL.
* **Prudence publicitaire :** Ignorez systématiquement les liens « Sponsorisés » (annonces) dans les moteurs de recherche pour le téléchargement d'outils techniques.
* **Inspection :** N'exécutez jamais une commande de script trouvée en ligne sans analyser son contenu au préalable.
* **Bonnes pratiques :** Mettez en favori les portails de téléchargement officiels pour éviter d'utiliser un moteur de recherche à chaque nouvelle installation.

---
[Source](https://www.bleepingcomputer.com/news/security/fake-claude-code-install-guides-push-infostealers-in-installfix-attacks/){:target="_blank"}
