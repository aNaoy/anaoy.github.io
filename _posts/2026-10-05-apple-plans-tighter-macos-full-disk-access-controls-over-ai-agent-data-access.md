---
title: 'Apple Plans Tighter macOS Full Disk Access Controls Over AI Agent Data Access'
date: 2026-10-05
permalink: /posts/2026/10/05/apple-plans-tighter-macos-full-disk-access-controls-over-ai-agent-data-access/
tags:
- veille-cyber
- hackernews
---
### Renforcement de la sécurité des accès disque sur macOS face aux agents IA

Apple prévoit de restreindre davantage le paramètre « Accès complet au disque » (Full Disk Access - FDA) sur macOS. Cette mesure vise à limiter les risques liés aux agents d'intelligence artificielle qui, une fois autorisés, peuvent accéder sans restriction aux fichiers système, e-mails, messages et historiques de navigation, souvent au-delà de ce que l'utilisateur anticipe.

**Points clés :**
* **Évolution des risques :** La nature autonome des agents IA augmente considérablement la surface d'attaque en cas de compromission.
* **Problématique des privilèges :** Le FDA permet aux applications de contourner les mesures de sécurité standard. Les chercheurs ont démontré que des outils comme l'agent *Muse* de Meta peuvent être détournés pour exploiter ces privilèges élevés.
* **Risque d'escalade :** Les vulnérabilités au sein d'applications d'IA permettent à des processus locaux non privilégiés d'usurper l'identité de l'IA ou d'abuser de ses autorisations (accès au micro, caméra, données personnelles).

**Vulnérabilités notables :**
* **CVE-2026-100754 :** Faille dans l'application ChatGPT pour Mac permettant à un attaquant de prendre le contrôle de l'assistant et de dérober l'historique des conversations.
* **Exploit « not-a-mused » (Muse) :** Exploitation d'un paramètre non documenté (`endo_voyager_dictation_endpoint`) permettant de capturer des dictées audio, d'injecter des commandes malveillantes et d'abuser des privilèges système accordés à l'application.

**Recommandations :**
* **Prudence accrue :** Ne pas accorder l'accès complet au disque à des outils d'IA, sauf nécessité absolue et confiance totale envers l'éditeur.
* **Gestion des autorisations :** Auditer régulièrement la liste des applications disposant de l'« Accès complet au disque » dans les paramètres *Confidentialité et sécurité* de macOS.
* **Veille aux mises à jour :** Appliquer immédiatement les correctifs fournis par les éditeurs d'applications d'IA pour limiter les risques liés à l'exécution de code local ou au détournement de jetons d'authentification.

---
[Source](https://thehackernews.com/2026/10/apple-plans-tighter-macos-full-disk.html){:target="_blank"}
