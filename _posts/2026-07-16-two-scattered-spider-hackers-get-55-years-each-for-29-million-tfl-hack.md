---
title: 'Two Scattered Spider Hackers Get 5.5 Years Each for £29 Million TfL Hack'
date: 2026-07-16
permalink: /posts/2026/07/16/two-scattered-spider-hackers-get-55-years-each-for-29-million-tfl-hack/
tags:
- veille-cyber
- hackernews
---
### Condamnation historique pour le piratage massif de TfL par Scattered Spider

Deux membres éminents du groupe de cybercriminels « Scattered Spider » (aussi connu sous le nom d'Octo Tempest), Owen Flowers et Thalha Jubair, ont été condamnés à 5 ans et demi de prison chacun au Royaume-Uni. Ils sont les premiers individus condamnés sous l'article 3ZA du *Computer Misuse Act 1990* pour avoir causé un risque grave au bien-être public lors de l'attaque de Transport for London (TfL) en septembre 2024.

**Points clés :**
*   **Impact de l'attaque :** L'intrusion a paralysé 148 systèmes de TfL, compromis les données personnelles de milliers d'usagers (y compris des coordonnées bancaires) et engendré 29 millions de livres sterling de coûts de récupération.
*   **Mode opératoire :** Le groupe privilégie l'ingénierie sociale, le *SIM swapping* et le hameçonnage pour capturer les accès SSO et les codes MFA.
*   **Récidive :** Lors de son arrestation, Flowers était en train de cibler des infrastructures de santé américaines (SSM Health, Sutter Health), menaçant explicitement la vie des patients.
*   **Procédure judiciaire :** Jubair fait également l'objet de poursuites aux États-Unis pour une centaine d'intrusions, avec des enjeux financiers dépassant 115 millions de dollars de rançons cumulées.

**Vulnérabilités exploitées :**
L'article ne mentionne pas de CVE spécifique, mais souligne l'exploitation des processus manuels de gestion des identités :
*   **Ingénierie sociale (Vishing) :** Manipulation des employés pour contourner les procédures de réinitialisation de mot de passe et d'inscription d'appareils MFA.
*   **Failles procédurales :** Abus des flux de travail manuels permettant d'enregistrer de nouveaux dispositifs pour les accès multifacteurs.

**Recommandations :**
*   **Renforcement de l'identité :** Appliquer une vérification rigoureuse de l'identité humaine lors de toute demande de réinitialisation de mot de passe, de modification de paramètres MFA ou d'enrôlement d'un nouvel appareil.
*   **Culture de signalement :** Les autorités soulignent que la coopération précoce avec les forces de l'ordre est déterminante pour l'efficacité des enquêtes et l'identification des coupables.
*   **Sécurisation SaaS :** Adopter des mesures de durcissement (hardening) spécifiques aux services cloud et SaaS pour contrer les tactiques d'extorsion modernes.

---
[Source](https://thehackernews.com/2026/07/two-scattered-spider-hackers-get-55.html){:target="_blank"}
