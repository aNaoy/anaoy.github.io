---
title: 'UK fines LastPass over 2022 data breach impacting 1.6 million users'
date: 2025-12-11
permalink: /posts/2025/12/11/uk-fines-lastpass-over-2022-data-breach-impacting-16-million-users/
tags:
- veille-cyber
- bleepingcomp
---
LastPass sanctionné pour une faille de sécurité de 2022

La société de gestion de mots de passe LastPass a été condamnée à une amende de 1,2 million de livres sterling par le Information Commissioner's Office (ICO) du Royaume-Uni. Cette sanction fait suite à une violation de données survenue en 2022, qui a permis à un attaquant de dérober des informations personnelles et des coffres-forts de mots de passe chiffrés appartenant à près de 1,6 million d'utilisateurs britanniques.

L'incident s'est déroulé en deux phases. Initialement, un pirate a compromis l'ordinateur portable d'un employé de LastPass, accédant ainsi à l'environnement de développement de l'entreprise. Bien qu'aucune donnée personnelle n'ait été volée à ce stade, le code source, des informations techniques propriétaires et des identifiants chiffrés ont été dérobés. La faille s'est aggravée lorsque l'attaquant a ciblé un employé senior en exploitant une vulnérabilité connue d'une application tierce (probablement Plex) installée sur son appareil personnel. Ce piratage a permis de récupérer le mot de passe maître de l'employé, contournant l'authentification multifacteur.

L'utilisation du même mot de passe maître pour ses comptes personnels et professionnels a donné à l'attaquant accès au coffre-fort professionnel, lui permettant de voler une clé d'accès Amazon Web Services et une clé de déchiffrement. Ces éléments, combinés aux informations précédemment obtenues, ont permis aux pirates de pénétrer le stockage cloud de GoTo et de dérober des sauvegardes de bases de données de LastPass.

Les données dérobées comprenaient les coffres-forts de mots de passe chiffrés, les noms, adresses e-mail, numéros de téléphone et URLs de sites web des clients. Bien que le ICO ait précisé que les coffres-forts eux-mêmes n'ont pas été déchiffrés par l'attaquant grâce à l'architecture "Zero Knowledge" de LastPass, la sécurité de ces coffres dépendait de la force des mots de passe maîtres des utilisateurs. Des chercheurs suggèrent que des coffres-forts utilisant des mots de passe faibles auraient pu être compromis par des attaques par force brute.

Points clés :

*   Amende de 1,2 million de livres sterling infligée à LastPass par l'ICO.
*   Violation de données ayant affecté 1,6 million d'utilisateurs britanniques en 2022.
*   Compromission initiale de l'ordinateur d'un employé, puis exploitation d'une vulnérabilité tierce sur un appareil personnel.
*   Vol de code source, d'informations techniques, d'identifiants et de sauvegardes de bases de données.
*   Dérober des informations personnelles incluant des coffres-forts de mots de passe chiffrés, noms, adresses e-mail, numéros de téléphone.
*   Sécurité des coffres-forts dépendant de la complexité du mot de passe maître de l'utilisateur.

Vulnérabilités :

*   Vulnérabilité dans une application de streaming tierce (probablement Plex) exploitée sur un appareil personnel.
*   Utilisation du même mot de passe maître pour des comptes personnels et professionnels.
*   Vulnérabilité potentielle des mots de passe maîtres faibles aux attaques par force brute (non spécifié avec CVE).

Recommandations :

*   Les entreprises doivent renforcer leurs contrôles d'accès et leurs systèmes internes contre les attaques ciblées.
*   Les utilisateurs doivent utiliser des mots de passe maîtres forts et complexes (au moins 16 caractères, incluant majuscules, minuscules, chiffres, symboles et caractères spéciaux) ou de longues phrases de passe pour protéger les informations sensibles comme les coffres-forts de mots de passe.
*   Les entreprises sont encouragées à revoir la sécurité de leurs appareils, les risques liés au travail à distance et les restrictions d'accès.

---
[Source](https://www.bleepingcomputer.com/news/security/uk-fines-lastpass-over-2022-data-breach-impacting-16-million-users/){:target="_blank"}
