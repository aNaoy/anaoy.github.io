---
title: 'Tomiris Shifts to Public-Service Implants for Stealthier C2 in Attacks on Government Targets'
date: 2025-12-01
permalink: /posts/2025/12/01/tomiris-shifts-to-public-service-implants-for-stealthier-c2-in-attacks-on-government-targets/
tags:
- veille-cyber
- hackernews
---
**L'acteur malveillant Tomiris cible les gouvernements avec des implants furtifs**

Tomiris, un acteur de menaces ciblant des ministères étrangers, des organisations intergouvernementales et des entités gouvernementales en Russie, a adopté une nouvelle stratégie pour ses opérations de commande et contrôle (C2). Les chercheurs de Kaspersky ont observé une utilisation accrue d'implants exploitant des services publics tels que Telegram et Discord pour le C2, dans le but de masquer le trafic malveillant dans l'activité légitime des services et d'éviter la détection. Les attaques se caractérisent par des courriels d'hameçonnage ciblant spécifiquement des utilisateurs russophones et des entités dans des pays d'Asie centrale, utilisant du contenu adapté dans les langues nationales respectives.

**Points Clés:**

*   **Changement Tactique:** Utilisation accrue d'implants exploitant des services publics (Telegram, Discord) pour le C2.
*   **Ciblage:** Ministères des affaires étrangères, organisations intergouvernementales, entités gouvernementales en Russie et en Asie centrale (Turkménistan, Kirghizistan, Tadjikistan, Ouzbékistan).
*   **Méthodes d'Accès Initial:** Courriels d'hameçonnage contenant des archives RAR protégées par mot de passe, avec le mot de passe inclus dans le corps de l'e-mail.
*   **Architecture:** Combinaison de reverse shells, d'implants personnalisés et de frameworks C2 open-source comme Havoc et AdaptixC2 pour la post-exploitation.
*   **Diversité des Implants:** Utilisation de divers implants écrits en C++, C#, Rust et Go, exploitant Telegram et Discord pour le C2.
*   **Persistance:** Modifications du registre Windows pour assurer la persistance des charges utiles.
*   **Identification:** Liens hypothétiques avec des clusters tels que Storm-0473, Cavalry Werewolf, ShadowSilk, Silent Lynx, SturgeonPhisher et YoroTrooper.

**Vulnérabilités:**

L'article ne mentionne pas de CVE spécifiques, mais les méthodes d'attaque reposent sur l'ingénierie sociale (hameçonnage) et l'exploitation de fonctionnalités de plateformes de communication légitimes pour le C2. Les vulnérabilités implicites sont liées à la manière dont les organisations gèrent la sécurité de leurs e-mails, la formation de leurs employés face à l'hameçonnage, et la surveillance de leur trafic réseau pour détecter les communications anormales, même lorsqu'elles utilisent des services populaires.

**Recommandations:**

*   **Renforcer la vigilance face à l'hameçonnage:** Former les employés à identifier et signaler les courriels suspects, en particulier ceux contenant des pièces jointes inattendues ou des demandes inhabituelles.
*   **Surveillance du trafic réseau:** Mettre en place des systèmes de détection et de prévention des intrusions capables de surveiller les communications sortantes vers des services publics comme Telegram et Discord pour détecter des comportements anormaux, même si le trafic est chiffré.
*   **Segmentation du réseau:** Isoler les systèmes critiques pour limiter la portée d'une éventuelle compromission.
*   **Gestion des accès:** Appliquer le principe du moindre privilège pour limiter les dommages potentiels en cas de compromission d'un compte.
*   **Utilisation d'outils de sécurité avancés:** Déployer des solutions de sécurité capables d'analyser le comportement des malwares et de détecter les techniques d'évasion.
*   **Mise à jour régulière des systèmes:** S'assurer que tous les systèmes d'exploitation et logiciels sont à jour pour corriger les vulnérabilités connues.

---
[Source](https://thehackernews.com/2025/12/tomiris-shifts-to-public-service.html){:target="_blank"}
