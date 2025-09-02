---
title: 'Malicious npm Package nodejs-smtp Mimics Nodemailer, Targets Atomic and Exodus Wallets'
date: 2025-09-02
permalink: /posts/2025/09/02/malicious-npm-package-nodejs-smtp-mimics-nodemailer-targets-atomic-and-exodus-wallets/
tags:
- veille-cyber
- hackernews
---
**Faux paquet npm : un leurre pour voler des cryptomonnaies**

Un paquet npm malveillant nommé `nodejs-smtp` a été découvert. Il imite la bibliothèque légitime `nodemailer` avec une présentation identique afin de tromper les développeurs. Ce paquet, qui n'est plus disponible, a été utilisé pour cibler des applications de portefeuille de cryptomonnaies pour Windows, telles qu'Atomic et Exodus.

Une fois importé, le paquet exploite les outils Electron pour décompresser les archives `app.asar` des applications ciblées. Il remplace ensuite un composant interne par une charge utile malveillante, reconditionne l'application modifiée et supprime ses traces.

L'objectif principal est de rediriger les transactions de diverses cryptomonnaies (Bitcoin, Ethereum, Tether, XRP, Solana) vers des portefeuilles contrôlés par les attaquants, agissant ainsi comme un "clippeur" de cryptomonnaies. Le paquet conserve sa fonctionnalité d'envoi d'e-mails pour ne pas éveiller les soupçons. Cette méthode permet de modifier discrètement une application de bureau existante sur un poste de travail compromis, même après redémarrages.

**Points Clés :**

*   Découverte d'un paquet npm malveillant : `nodejs-smtp`.
*   Ce paquet imite `nodemailer`.
*   Il cible les portefeuilles de cryptomonnaies pour Windows : Atomic et Exodus.
*   Le mécanisme utilise Electron pour modifier les fichiers internes des applications ciblées.
*   L'objectif est de rediriger les fonds vers des portefeuilles contrôlés par les attaquants (clippeur de cryptomonnaies).
*   La fonctionnalité d'envoi d'e-mails sert de couverture pour dissimuler l'activité malveillante.

**Vulnérabilités :**

Aucun identifiant CVE spécifique n'est mentionné dans l'article pour cette attaque.

**Recommandations :**

*   Vérifier scrupuleusement les dépendances npm importées, en particulier leur nom et leur provenance.
*   Se méfier des paquets qui imitent des bibliothèques légitimes.
*   Effectuer des analyses de sécurité régulières sur le code source et les dépendances des applications.
*   Être vigilant quant aux changements inattendus dans le comportement des applications de portefeuille de cryptomonnaies.

---
[Source](https://thehackernews.com/2025/09/malicious-npm-package-nodejs-smtp.html){:target="_blank"}
