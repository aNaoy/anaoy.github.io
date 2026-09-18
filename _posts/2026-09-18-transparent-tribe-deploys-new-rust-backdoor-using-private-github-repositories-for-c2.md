---
title: 'Transparent Tribe Deploys New Rust Backdoor Using Private GitHub Repositories for C2'
date: 2026-09-18
permalink: /posts/2026/09/18/transparent-tribe-deploys-new-rust-backdoor-using-private-github-repositories-for-c2/
tags:
- veille-cyber
- hackernews
---
### Opération RapidRust : Nouvelle offensive cyber du groupe APT36

Le groupe de menace Transparent Tribe (APT36), affilié au Pakistan, mène actuellement une campagne d'espionnage baptisée « Operation RapidRust ». Ciblant principalement des entités gouvernementales et de défense en Inde et en Afghanistan, les attaquants utilisent un arsenal de logiciels malveillants récents développés en Rust et des techniques de contournement sophistiquées.

**Points clés :**
* **Infrastructures détournées :** Les attaquants exploitent des dépôts GitHub privés pour le commandement et le contrôle (C2), utilisant l'API REST de GitHub pour échanger des commandes chiffrées sans éveiller de soupçons.
* **Typosquatting :** Utilisation de domaines usurpant des médias indiens reconnus (*theprints[.]org* et *indiatodays[.]org*) pour héberger des scripts malveillants.
* **Nouvel arsenal :**
    * **RUSTYSHADE :** Backdoor en Rust permettant la capture d'écran, l'accès webcam et l'exécution de commandes.
    * **RUSTYMOVE :** Outil de propagation via clés USB sur Windows.
    * **PSNATCH / BASHNATCH :** Outils de vol de données (stealers) ciblant les documents sensibles sur Windows et Linux.
* **Mode opératoire :** Les activités malveillantes sont minutieusement planifiées, avec une communication C2 restreinte aux jours de semaine, entre 4h et 11h UTC.

**Vulnérabilités :**
* Aucune CVE spécifique n'est exploitée ; l'attaque repose sur l'exécution de scripts PowerShell et de binaires malveillants après une compromission initiale, ainsi que sur l'ingénierie sociale (fichiers LNK déguisés en PDF).

**Recommandations :**
* **Surveillance réseau :** Bloquer les connexions sortantes vers des dépôts GitHub non autorisés ou suspects, particulièrement ceux utilisés pour le transfert de fichiers (`command.txt`, `results.txt`, etc.).
* **Contrôle des périphériques :** Restreindre ou désactiver l'exécution automatique (AutoRun) des clés USB pour contrer les outils de propagation comme RUSTYMOVE.
* **Sécurité des endpoints :** Déployer des solutions EDR capables de détecter l'exécution de scripts PowerShell suspicieux et de surveiller les processus utilisant des API GitHub pour des échanges de données inhabituels.
* **Sensibilisation :** Alerter les utilisateurs sur les risques liés aux téléchargements depuis des sites web d'actualités aux URL légèrement modifiées (typosquatting).

---
[Source](https://thehackernews.com/2026/09/transparent-tribe-deploys-new-rust.html){:target="_blank"}
