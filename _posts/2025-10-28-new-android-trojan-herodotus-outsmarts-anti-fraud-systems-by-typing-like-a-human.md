---
title: 'New Android Trojan Herodotus Outsmarts Anti-Fraud Systems by Typing Like a Human'
date: 2025-10-28
permalink: /posts/2025/10/28/new-android-trojan-herodotus-outsmarts-anti-fraud-systems-by-typing-like-a-human/
tags:
- veille-cyber
- hackernews
---
### Herodotus : Un nouveau cheval de Troie Android simule un comportement humain pour déjouer les systèmes antifraude

Un nouveau logiciel malveillant de type cheval de Troie bancaire Android, baptisé **Herodotus**, est actif et cible l'Italie et le Brésil pour des attaques de prise de contrôle d'appareils (Device Takeover - DTO). Sa particularité réside dans sa capacité à imiter le comportement humain pour échapper aux systèmes de détection basés sur la biométrie comportementale.

Ce logiciel malveillant, proposé sous un modèle de "malware-as-a-service" (MaaS), fonctionne sur les appareils Android des versions 9 à 16. Bien qu'il ne soit pas une évolution directe du cheval de Troie Brokewell, il en emprunte certaines techniques, notamment dans l'obfuscation du code.

Herodotus exploite les services d'accessibilité Android pour interagir avec l'écran, afficher des écrans de connexion frauduleux par-dessus les applications bancaires légitimes afin de voler les identifiants. Il est également capable de voler les codes d'authentification à deux facteurs (2FA) envoyés par SMS, d'intercepter ce qui s'affiche à l'écran, d'obtenir le schéma ou le code PIN de déverrouillage, et d'installer des fichiers APK à distance.

Sa principale innovation consiste à introduire des délais aléatoires (entre 300 et 3000 millisecondes) lors de la saisie de texte, simulant ainsi la façon dont un utilisateur humain taperait. Cette technique vise à éviter la détection par les solutions antifraude qui repèrent une vitesse de saisie typique des machines.

Le développement d'Herodotus est actif et ses opérateurs étendent leur portée, ciblant des organisations financières aux États-Unis, en Turquie, au Royaume-Uni et en Pologne, ainsi que des portefeuilles et des plateformes d'échange de cryptomonnaies.

**Points clés :**

*   Nouveau cheval de Troie bancaire Android : Herodotus.
*   Ciblage : Italie, Brésil (et expansion vers États-Unis, Turquie, Royaume-Uni, Pologne).
*   Méthode d'attaque : Prise de contrôle d'appareils (DTO), vol d'identifiants bancaires.
*   Technique d'évasion : Simule le comportement humain par des délais aléatoires dans la saisie de texte.
*   Exploitation : Services d'accessibilité Android pour des actions malveillantes.
*   Fonctionnalités : Vol d'identifiants, interception de SMS 2FA, obtention du schéma de déverrouillage, installation d'APK à distance.
*   Distribution : via des applications dropper déguisées en Google Chrome, par hameçonnage SMS ou ingénierie sociale.
*   Liens avec d'autres malwares : Emprunte des techniques à Brokewell.

**Vulnérabilités (sans CVE spécifique mentionné dans l'article) :**

*   L'exploitation des services d'accessibilité Android.
*   Les vulnérabilités dans les systèmes antifraude basés sur la biométrie comportementale et la détection de la vitesse de saisie.

**Recommandations :**

*   Se méfier des applications provenant de sources inconnues et des liens reçus par SMS.
*   Être vigilant quant aux demandes d'autorisations excessives par les applications.
*   Maintenir les systèmes d'exploitation et les applications à jour.
*   Utiliser des solutions de sécurité mobile fiables.

---
[Source](https://thehackernews.com/2025/10/new-android-trojan-herodotus-outsmarts.html){:target="_blank"}
