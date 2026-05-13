---
title: 'US govt seeks Instructure testimony on massive Canvas cyberattack'
date: 2026-05-13
permalink: /posts/2026/05/13/us-govt-seeks-instructure-testimony-on-massive-canvas-cyberattack/
tags:
- veille-cyber
- bleepingcomp
---
### Enquête parlementaire sur les cyberattaques massives contre la plateforme Canvas

La commission de la sécurité intérieure de la Chambre des représentants des États-Unis a sommé la direction d'Instructure de s'expliquer suite à deux cyberattaques majeures perpétrées par le groupe de cybercriminels « ShinyHunters ». Ces intrusions ont compromis la plateforme d'apprentissage Canvas, affectant des millions d'utilisateurs et perturbant les examens finaux de milliers d'établissements scolaires.

**Points clés :**
*   **Double intrusion :** Instructure a subi deux attaques en l'espace d'une semaine fin avril 2024.
*   **Vol de données :** Le groupe ShinyHunters affirme avoir dérobé 280 millions d'enregistrements (noms, e-mails, identifiants étudiants, messages privés) provenant de plus de 8 800 institutions éducatives. Aucun mot de passe ou donnée financière n'aurait été compromis.
*   **Sabotage :** La seconde attaque a consisté en une défiguration (defacement) des portails de connexion, entraînant l'annulation d'examens dans plusieurs États américains.
*   **Accord de résolution :** Instructure a confirmé avoir conclu un accord avec le groupe pour faire supprimer les données volées, suggérant le paiement d'une rançon, bien que l'entreprise reste évasive sur les termes exacts.
*   **Contrôle parlementaire :** Le Congrès exige une audition avant le 21 mai pour évaluer la réactivité de l'entreprise et ses pratiques de protection des données.

**Vulnérabilités :**
*   **Exploitation de failles XSS (Cross-Site Scripting) :** Les attaquants ont utilisé plusieurs vulnérabilités de type XSS pour usurper des sessions administrateur authentifiées et modifier les pages de connexion. Aucune CVE spécifique n'est mentionnée dans le rapport initial, ces vulnérabilités étant internes à la configuration ou au développement de la plateforme.

**Recommandations :**
*   **Renforcement des sessions :** Sécuriser davantage la gestion des sessions administrateur pour contrer les attaques par injection de scripts.
*   **Transparence et audit :** Instructure est sous pression pour fournir un rapport détaillé sur son plan de remédiation, ses capacités de détection d'intrusions et sa stratégie de réponse aux incidents.
*   **Vigilance institutionnelle :** Les établissements scolaires utilisant des plateformes LMS (Learning Management System) doivent auditer leurs accès, renforcer l'authentification multifacteur (MFA) pour les comptes à privilèges et surveiller toute activité suspecte sur leurs portails de connexion.

---
[Source](https://www.bleepingcomputer.com/news/security/us-govt-seeks-instructure-testimony-on-massive-canvas-cyberattack/){:target="_blank"}
