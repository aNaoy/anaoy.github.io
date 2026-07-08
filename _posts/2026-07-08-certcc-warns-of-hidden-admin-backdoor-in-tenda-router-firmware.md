---
title: 'CERT/CC Warns of Hidden Admin Backdoor in Tenda Router Firmware'
date: 2026-07-08
permalink: /posts/2026/07/08/certcc-warns-of-hidden-admin-backdoor-in-tenda-router-firmware/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique : Backdoor dans le firmware des routeurs Tenda

Le CERT/CC a émis une alerte concernant la présence d'une porte dérobée (backdoor) non documentée dans plusieurs versions du firmware des routeurs Tenda, permettant un accès administratif total sans mot de passe valide.

**Points clés :**
* **Mécanisme d'attaque :** La vulnérabilité réside dans la fonction `login()` du binaire `/bin/httpd`. En cas d'échec de l'authentification standard, le système compare le mot de passe fourni par l'utilisateur avec une valeur stockée en clair dans la configuration du routeur (`sys.rzadmin.password`).
* **Accès non autorisé :** Le nom d'utilisateur n'est pas vérifié, ce qui permet à tout attaquant d'obtenir des privilèges administratifs complets en utilisant le mot de passe dérobé.
* **Absence de correctif :** À ce jour, Tenda n'a pas publié de mise à jour pour corriger cette faille.

**Vulnérabilité identifiée :**
* **CVE-2026-11405** : Permet le contournement de l'authentification et une prise de contrôle totale du périphérique.

**Modèles de firmware impactés :**
* US_FH1201V1.0BR_V1.2.0.14(408)_EN_TD
* US_W15EV1.0br_V15.11.0.5(1068_1567_841)_EN_TDE
* US_AC10V1.0re_V15.03.06.46_multi_TDE01
* US_AC5V1.0RTL_V15.03.06.48_multi_TDE01
* US_AC6V2.0RTL_V15.03.06.51_multi_T

**Recommandations :**
* Désactiver immédiatement la gestion à distance (Remote Management) sur les routeurs concernés.
* Modifier l'adresse IP par défaut du réseau local (LAN) pour limiter la visibilité face aux scans automatisés.

---
[Source](https://thehackernews.com/2026/07/certcc-warns-of-hidden-admin-backdoor.html){:target="_blank"}
