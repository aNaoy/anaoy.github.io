---
title: 'On the Security of Password Managers'
date: 2026-02-24
permalink: /posts/2026/02/24/on-the-security-of-password-managers/
tags:
- veille-cyber
- schneier
---
**Gérer ses mots de passe : les failles cachées des gestionnaires cloud**

Une nouvelle étude révèle que certains gestionnaires de mots de passe, malgré leurs promesses, ne garantissent pas l'inaccessibilité de leurs coffres-forts aux opérateurs de serveurs. Cette situation peut se produire notamment lors de l'utilisation de fonctions de récupération de compte, de partage de coffres-forts ou de regroupement d'utilisateurs.

En analysant Bitwarden, Dashlane et LastPass, les chercheurs ont identifié des méthodes permettant à une personne contrôlant le serveur, que ce soit par administration ou suite à une compromission, de dérober des données, y compris des coffres-forts entiers. De plus, d'autres attaques ont été développées pour affaiblir le chiffrement, rendant possible la conversion du texte chiffré en texte clair.

**Points clés :**

*   Les fonctions de récupération de compte, de partage et de regroupement peuvent affaiblir la sécurité des coffres-forts.
*   Les opérateurs de serveurs ou des acteurs malveillants ayant accès aux serveurs peuvent potentiellement accéder aux données.
*   Des vulnérabilités permettent d'affaiblir le chiffrement et de décrypter les données.

**Vulnérabilités (CVE non spécifiées dans l'article) :**

*   Accès aux données et coffres-forts par des tiers contrôlant les serveurs.
*   Possibilité d'affaiblir le chiffrement pour accéder aux données en clair.

**Recommandations :**

*   Être vigilant quant aux fonctionnalités de récupération et de partage proposées par les gestionnaires de mots de passe.
*   Pour une sécurité maximale, privilégier des solutions de gestion de mots de passe qui ne dépendent pas du cloud et qui n'offrent pas de fonctionnalités de récupération. L'article mentionne Password Safe comme une alternative sans cloud et sans fonctionnalités de récupération.

---
[Source](https://www.schneier.com/blog/archives/2026/02/on-the-security-of-password-managers.html){:target="_blank"}
