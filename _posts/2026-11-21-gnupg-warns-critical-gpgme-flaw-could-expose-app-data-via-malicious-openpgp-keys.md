---
title: 'GnuPG Warns Critical GPGME Flaw Could Expose App Data via Malicious OpenPGP Keys'
date: 2026-11-21
permalink: /posts/2026/11/21/gnupg-warns-critical-gpgme-flaw-could-expose-app-data-via-malicious-openpgp-keys/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans GPGME : Risque d'exposition de données via OpenPGP

Une faille critique a été identifiée dans la bibliothèque **GPGME**, utilisée par de nombreux logiciels pour interagir avec GnuPG. Un identifiant utilisateur (User ID) anormalement long au sein d'une clé OpenPGP malveillante peut déclencher une corruption mémoire, exposant potentiellement les données des applications ou permettant l'exécution de code à distance.

**Points clés :**
*   **Nature de la faille :** Il s'agit d'une vulnérabilité de type « double free » (double libération mémoire) située dans les routines `read_status()` et `read_colon_line()`.
*   **Impact :** La faille affecte une large gamme de logiciels, incluant des clients mail, des clients XMPP, Samba, ainsi que les suites Gpg4win et GnuPG Desktop.
*   **État de la menace :** Aucune exploitation active n'a été signalée, mais le risque d'exécution de code arbitraire ne peut être exclu.

**Vulnérabilité :**
*   **CVE-2026-129975**

**Recommandations :**
*   **Mise à jour immédiate :** Passer à la version **GPGME 2.3.1**.
*   **Utilisateurs Windows :** Installer la version **Gpg4win 5.1.2** qui intègre la bibliothèque corrigée.
*   **Versions obsolètes :** Pour les systèmes ne pouvant migrer vers la version 2.3.1, utiliser la version **1.24.4** ou appliquer le correctif fourni dans l'avis de sécurité officiel.
*   **Logiciels liés statiquement :** Les applications intégrant GPGME nativement doivent impérativement être recompilées avec la bibliothèque mise à jour, car une simple mise à jour système ne suffira pas.
*   **Absence de contournement :** Aucun mécanisme de protection temporaire n'est disponible ; seule la mise à jour logicielle permet de neutraliser la faille.

---
[Source](https://thehackernews.com/2026/11/gnupg-warns-critical-gpgme-flaw-could.html){:target="_blank"}
