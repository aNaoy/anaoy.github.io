---
title: 'APT28-Linked Campaign Deploys BadPaw Loader and MeowMeow Backdoor in Ukraine'
date: 2026-03-05
permalink: /posts/2026/03/05/apt28-linked-campaign-deploys-badpaw-loader-and-meowmeow-backdoor-in-ukraine/
tags:
- veille-cyber
- hackernews
---
Campagne Russe en Ukraine : Déploiement de BadPaw et MeowMeow

Une campagne cybernétique d'origine russe vise des entités ukrainiennes via une chaîne d'attaque débutant par un email de phishing. Ce dernier contient un lien vers une archive ZIP. Après extraction, un fichier HTA affiche un document trompeur en ukrainien sur des appels de franchissement de frontière. Parallèlement, un chargeur .NET nommé BadPaw est déployé. Il établit ensuite la communication avec un serveur distant pour télécharger et exécuter une porte dérobée sophistiquée, MeowMeow.

Cette campagne est attribuée avec une confiance modérée au groupe APT28, en raison du ciblage, de la nature géopolitique des leurres et des similitudes avec des opérations russes antérieures.

Points clés :
*   **Phishing ciblé :** Les emails proviennent de ukr[.]net pour renforcer la crédibilité.
*   **Attaque en plusieurs étapes :** Un premier lien sert de pixel de suivi, redirigeant vers le téléchargement de l'archive ZIP.
*   **Ingénierie sociale :** Un document leurre sur le franchissement de frontière est affiché pour tromper la victime.
*   **Désactivation des analyses automatisées :** Le malware vérifie l'ancienneté de l'installation du système d'exploitation (plus de 10 jours) et la présence d'outils d'analyse pour éviter les sandbox.
*   **Persistance :** Un script VBS est créé via une tâche planifiée pour assurer la persistance.
*   **Code malveillant caché :** Le code de BadPaw est intégré dans une image PNG.
*   **Leurres fonctionnels :** BadPaw affiche une interface avec un chat si exécuté indépendamment, et MeowMeow affiche "Meow Meow Meow" pour détourner l'analyse manuelle.
*   **Langage russe dans le code :** La présence de chaînes de caractères en russe suggère une erreur d'OPSEC ou des artefacts de développement.

Vulnérabilités :
*   Aucune CVE spécifique n'est mentionnée dans l'article. Les vulnérabilités exploitées sont liées à l'ingénierie sociale et à l'exécution de code arbitraire après l'ouverture de fichiers compromis.

Recommandations :
*   **Vigilance accrue :** Être prudent face aux emails de phishing, même s'ils proviennent de sources apparemment fiables.
*   **Vérification des liens et des pièces jointes :** Ne pas cliquer sur des liens suspects ou ouvrir des archives non sollicitées.
*   **Sensibilisation :** Former les utilisateurs à reconnaître les tactiques de phishing et d'ingénierie sociale.
*   **Surveillance des activités suspectes :** Mettre en place une surveillance des réseaux et des systèmes pour détecter les comportements anormaux.
*   **Mises à jour et correctifs :** Maintenir les systèmes et les logiciels à jour pour atténuer les vulnérabilités connues (bien qu'aucune spécifique ne soit citée ici).

---
[Source](https://thehackernews.com/2026/03/apt28-linked-campaign-deploys-badpaw.html){:target="_blank"}
