---
title: 'CubePilot drone software dev hit by DNS hijacking to intercept traffic'
date: 2026-07-29
permalink: /posts/2026/07/29/cubepilot-drone-software-dev-hit-by-dns-hijacking-to-intercept-traffic/
tags:
- veille-cyber
- bleepingcomp
---
### Détournement DNS chez CubePilot : menaces sur les logiciels de drones

CubePilot, concepteur australien de systèmes de navigation pour drones, a été victime d'une attaque par détournement de DNS le 24 juillet. Les attaquants ont pris le contrôle des paramètres DNS du domaine `cubepilot.org`, permettant l'interception de données et l'usurpation de services légitimes via l'émission de certificats TLS frauduleux.

**Points clés :**
* **Interception de données :** Les utilisateurs ayant accédé au portail ou au forum pendant l'incident pourraient avoir vu leurs identifiants compromis.
* **Infrastructure compromise :** L'usage de certificats HTTPS valides a rendu l'attaque indétectable pour les utilisateurs finaux.
* **Intégrité logicielle :** Un risque potentiel existe sur les images de firmware téléchargées les 24 et 25 juillet.
* **Services impactés :** Le portail OEM, le forum, la documentation et le système ERP ont été mis hors ligne par mesure de sécurité.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée à cet incident, l'attaque reposant sur une compromission directe de la gestion des enregistrements DNS du domaine.

**Recommandations :**
* **Mots de passe :** Si les identifiants utilisés sur les services CubePilot sont identiques à ceux d'autres plateformes, changez-les immédiatement.
* **Firmware :** Ne pas installer de mises à jour de firmware téléchargées entre le 24 et le 25 juillet. Celles acquises avant le 24 juillet restent considérées comme sûres.
* **Paiements :** En cas de réception de demandes de paiement, vérifier systématiquement leur authenticité par téléphone auprès d'un contact habituel de l'entreprise.
* **Veille :** Surveiller les communications officielles de CubePilot pour la reprise sécurisée des services.

---
[Source](https://www.bleepingcomputer.com/news/security/cubepilot-drone-software-dev-hit-by-dns-hijacking-to-intercept-traffic/){:target="_blank"}
