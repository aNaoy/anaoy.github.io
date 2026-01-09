---
title: 'FBI warns about Kimsuky hackers using QR codes to phish U.S. orgs'
date: 2026-01-09
permalink: /posts/2026/01/09/fbi-warns-about-kimsuky-hackers-using-qr-codes-to-phish-us-orgs/
tags:
- veille-cyber
- bleepingcomp
---
**Le groupe Kimsuky utilise les QR codes pour des attaques par hameçonnage**

Le groupe de pirates informatiques nord-coréen Kimsuky, également connu sous le nom d'APT43, emploie des QR codes malveillants dans le cadre de campagnes de hameçonnage ciblant des organisations américaines. Ces attaques visent spécifiquement des entités impliquées dans des politiques, recherches et analyses liées à la Corée du Nord, incluant des ONG, des groupes de réflexion, des universités, des cabinets de conseil stratégique et des entités gouvernementales.

L'utilisation de QR codes dans les attaques par hameçonnage, appelée "quishing", n'est pas nouvelle mais demeure une méthode efficace pour contourner les mesures de sécurité. Les emails frauduleux contiennent des QR codes qui, une fois scannés par les victimes avec leurs appareils mobiles, redirigent vers des sites web malveillants déguisés en questionnaires, espaces de stockage sécurisés ou pages de connexion falsifiées. Les attaquants se font passer pour divers interlocuteurs tels que des investisseurs étrangers, des employés d'ambassades, des membres de groupes de réflexion ou des organisateurs de conférences.

Lorsqu'un utilisateur scanne le code QR, son appareil est potentiellement dirigé via une infrastructure contrôlée par l'attaquant, collectant des informations telles que l'agent utilisateur, le système d'exploitation, l'adresse IP, la taille de l'écran et la langue locale. Les pages de phishing imitent souvent des portails légitimes comme Microsoft 365, Okta, des VPN ou des services Google, dans le but de voler des identifiants de connexion ou des jetons d'authentification. Ces attaques sont particulièrement préoccupantes car elles permettent de contourner l'authentification multifacteur (MFA) en volant des jetons de session, et échappent aux solutions de sécurité traditionnelles basées sur les emails et la surveillance réseau, car elles proviennent d'appareils mobiles non gérés.

**Points Clés :**

*   Le groupe de hackers étatique nord-coréen Kimsuky utilise le "quishing" (hameçonnage par QR code).
*   Les cibles sont des organisations américaines travaillant sur des sujets liés à la Corée du Nord.
*   Les QR codes redirigent vers de fausses pages de connexion ou formulaires pour voler des identifiants et des jetons de session.
*   Cette méthode permet de contourner l'authentification multifacteur (MFA).
*   Les attaquants se font passer pour des personnes de confiance.

**Vulnérabilités :**

*   Les attaques exploitent la confiance des utilisateurs envers les QR codes.
*   La technique permet de contourner les solutions de sécurité email traditionnelles et la MFA.
*   Les attaques proviennent d'appareils mobiles non gérés, échappant à la détection et à la réponse par point de terminaison (EDR).
*   (Aucun CVE spécifique n'est mentionné dans l'article pour cette technique particulière, mais le groupe Kimsuky est connu pour exploiter des vulnérabilités connues et des attaques de la chaîne d'approvisionnement dans le passé.)

**Recommandations :**

*   Formation renforcée des employés sur la vérification des QR codes et les campagnes de hameçonnage.
*   Vérification systématique de la source des QR codes avant leur scan.
*   Mise en place et application de la gestion des appareils mobiles (MDM).
*   Renforcement et application rigoureuse de l'authentification multifacteur (MFA).
*   Signalement immédiat de toute attaque suspecte au FBI ou au portail IC3.

---
[Source](https://www.bleepingcomputer.com/news/security/fbi-warns-about-kimsuky-hackers-using-qr-codes-to-phish-us-orgs/){:target="_blank"}
