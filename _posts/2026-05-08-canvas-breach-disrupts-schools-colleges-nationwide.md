---
title: 'Canvas Breach Disrupts Schools & Colleges Nationwide'
date: 2026-05-08
permalink: /posts/2026/05/08/canvas-breach-disrupts-schools-colleges-nationwide/
tags:
- veille-cyber
- krebs
---
### Cyberattaque majeure contre la plateforme éducative Canvas

La plateforme d'apprentissage Canvas (éditée par Instructure) a subi une série d'attaques par extorsion menées par le groupe cybercriminel **ShinyHunters**. Le groupe a réussi à compromettre l'interface de connexion de la plateforme, affichant des demandes de rançon et menaçant de divulguer les données de 275 millions d'utilisateurs. Cette intrusion, qui s'inscrit dans une campagne de harcèlement de huit mois, a entraîné la mise hors ligne temporaire des services en pleine période d'examens.

**Points clés :**
* **Récurrence :** Il s'agit au moins de la troisième intrusion de ShinyHunters sur les systèmes d'Instructure en huit mois.
* **Impact :** Les données compromises incluent des noms, adresses e-mail, identifiants étudiants et des échanges de messagerie privée.
* **Modus Operandi :** ShinyHunters privilégie le *phishing* vocal et l'ingénierie sociale (usurpation d'identité d'employés informatiques) pour obtenir des accès privilégiés.
* **Escalade :** Les attaquants ont poussé les universités à négocier individuellement leur propre rançon, court-circuitant ainsi l'éditeur.

**Vulnérabilités :**
* L'attaque a exploité une faille spécifique au sein des comptes **"Free-for-Teacher"** de Canvas, utilisée comme vecteur d'accès principal. Aucune CVE n'a été spécifiquement assignée à cet incident à ce stade, la méthode reposant sur une exploitation répétée de vulnérabilités d'accès.

**Recommandations :**
* **Désactivation des vecteurs à risque :** Instructure a suspendu temporairement les comptes "Free-for-Teacher" pour colmater la faille exploitée.
* **Communication officielle :** Les institutions touchées doivent privilégier les canaux de communication directs avec Instructure plutôt que de se fier aux listes de victimes diffusées sur les réseaux sociaux.
* **Renforcement de l'authentification :** Face à l'utilisation fréquente du *phishing* vocal et de la compromission de SSO (comme observé sur d'autres cibles du groupe), les organisations doivent durcir leurs protocoles d'authentification multifacteur (MFA) et sensibiliser leurs équipes aux techniques d'ingénierie sociale.

---
[Source](https://krebsonsecurity.com/2026/05/canvas-breach-disrupts-schools-colleges-nationwide/){:target="_blank"}
