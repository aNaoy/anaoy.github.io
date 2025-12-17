---
title: 'APT28 Targets Ukrainian UKR-net Users in Long-Running Credential Phishing Campaign'
date: 2025-12-17
permalink: /posts/2025/12/17/apt28-targets-ukrainian-ukr-net-users-in-long-running-credential-phishing-campaign/
tags:
- veille-cyber
- hackernews
---
## Campagne de Phishing du Groupe APT28 : Cible UKR[.]net

Le groupe APT28, affilié à la direction principale du renseignement militaire russe (GRU), mène une campagne soutenue de vol d'identifiants ciblant les utilisateurs du service de messagerie et d'actualités ukrainien UKR[.]net. Cette activité, observée entre juin 2024 et avril 2025, s'inscrit dans une stratégie plus large de collecte d'informations menée par le groupe depuis le milieu des années 2000.

Les attaques récentes se caractérisent par l'utilisation de fausses pages de connexion imitant l'apparence de UKR[.]net. Ces pages sont hébergées sur des services légitimes (comme Mocky) et accessibles via des liens contenus dans des documents PDF distribués par email. Ces liens sont souvent raccourcis (via tiny[.]cc ou tinyurl[.]com) ou masqués derrière des sous-domaines sur des plateformes comme Blogger.

L'objectif est de piéger les victimes pour qu'elles saisissent leurs identifiants et codes d'authentification à deux facteurs (2FA). Le groupe utilise désormais des services de tunneling proxy (comme ngrok et Serveo) pour capturer et relayer les informations volées, une adaptation probable aux actions de démantèlement d'infrastructure menées début 2024.

Cette campagne souligne l'intérêt persistant du GRU à compromettre les identifiants des utilisateurs ukrainiens pour soutenir ses opérations de renseignement dans le contexte du conflit en cours.

**Points Clés :**

*   **Acteur de menace :** APT28 (également connu sous divers autres noms comme BlueDelta, Fancy Bear, etc.), groupe parrainé par l'État russe et suspecté d'être lié au GRU.
*   **Cible principale :** Utilisateurs du service UKR[.]net en Ukraine.
*   **Méthode principale :** Campagne de phishing ciblée pour le vol d'identifiants.
*   **Outils et techniques :** Utilisation de fausses pages de connexion, documents PDF malveillants, services de raccourcissement d'URL, plateformes d'hébergement gratuites (Blogger), et services de tunneling proxy (ngrok, Serveo).
*   **Objectif :** Collecte d'informations sensibles et d'identifiants pour soutenir les objectifs stratégiques russes.
*   **Période d'observation :** Juin 2024 - Avril 2025.

**Vulnérabilités :**

L'article ne mentionne pas de vulnérabilités spécifiques avec des identifiants CVE. L'attaque repose sur l'exploitation de l'ingénierie sociale et la confiance des utilisateurs dans des services légitimes pour collecter des identifiants et des codes 2FA.

**Recommandations :**

Bien que l'article ne fournisse pas de liste explicite de recommandations, les observations suggèrent les bonnes pratiques suivantes :

*   **Vigilance accrue face aux emails de phishing :** Les utilisateurs doivent être extrêmement prudents avec les emails inattendus, surtout ceux contenant des liens ou des pièces jointes.
*   **Vérification des URL :** Avant de cliquer sur un lien, vérifier attentivement l'URL pour détecter toute anomalie ou différence avec l'adresse attendue.
*   **Authentification à deux facteurs (2FA) :** Bien que les codes 2FA soient également ciblés dans cette campagne, une 2FA robuste reste une couche de sécurité essentielle.
*   **Attention aux fausses pages de connexion :** Être particulièrement méfiant lors de la saisie d'identifiants sur des pages qui semblent légèrement différentes de l'original ou qui sont accessibles via des liens non sollicités.
*   **Sensibilisation à la cybersécurité :** Des formations régulières sur les menaces de phishing et les meilleures pratiques de sécurité sont cruciales pour les utilisateurs.

---
[Source](https://thehackernews.com/2025/12/apt28-targets-ukrainian-ukr-net-users.html){:target="_blank"}
