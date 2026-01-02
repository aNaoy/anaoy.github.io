---
title: 'Trust Wallet links $8.5 million crypto theft to Shai-Hulud NPM attack'
date: 2026-01-02
permalink: /posts/2026/01/02/trust-wallet-links-85-million-crypto-theft-to-shai-hulud-npm-attack/
tags:
- veille-cyber
- bleepingcomp
---
**Le vol de crypto via une attaque sur Trust Wallet et la campagne Shai-Hulud**

Une attaque par le biais d'une extension web de Trust Wallet a conduit au vol d'environ 8,5 millions de dollars auprès de plus de 2 500 portefeuilles de cryptomonnaies. L'incident, survenu le 24 décembre, est suspecté d'être lié à une attaque plus large nommée Shai-Hulud, visant l'écosystème npm.

L'exploitation a débuté par la compromission des secrets de développeur GitHub de Trust Wallet, accordant un accès au code source de l'extension et à la clé API du Chrome Web Store (CWS). Ce vol de clé a permis aux attaquants de contourner le processus de publication standard et d'uploader une version malveillante (v2.68.0) de l'extension sur le Chrome Web Store. Cette version contenait un fichier JavaScript infecté qui dérobait des données sensibles des portefeuilles et permettait des transactions non autorisées. Les attaquants ont également enregistré des domaines frauduleux pour héberger le code malveillant.

La campagne Shai-Hulud, également connue sous le nom de Shai-Hulud 2.0, a touché le registre de paquets npm, exposant potentiellement des centaines de milliers de secrets de développeurs et de clés API. Cette campagne de type "supply chain" a commencé en septembre et a évolué en compromettant un grand nombre de paquets npm, qui contenaient du code malveillant conçu pour collecter des informations d'identification.

**Points Clés :**

*   Vol de 8,5 millions de dollars en cryptomonnaies via une extension web compromise.
*   Lien présumé avec l'attaque Shai-Hulud sur l'écosystème npm.
*   Exploitation des secrets de développeur GitHub et de la clé API du Chrome Web Store pour injecter du code malveillant.
*   Contournement des processus de validation de l'extension par les attaquants.
*   Impératif de vigilance face aux tentatives d'hameçonnage et aux arnaques post-incident.

**Vulnérabilités :**

*   Exposition des secrets de développeur GitHub.
*   Compromission de la clé API du Chrome Web Store (CWS).
*   Injection de code malveillant dans une version légitime de l'extension Trust Wallet (v2.68.0).
*   Absence de contrôle de sécurité suffisant sur le processus de publication des mises à jour de l'extension.
*   Vulnérabilités liées à la campagne Shai-Hulud concernant la sécurité des paquets npm et la gestion des secrets de développeurs (pas de CVE spécifique mentionné pour Trust Wallet, mais la nature de l'attaque est une compromission de chaîne d'approvisionnement logicielle).

**Recommandations :**

*   **Pour Trust Wallet (actions déjà entreprises) :**
    *   Révocation de toutes les API de publication pour bloquer de nouvelles mises à jour malveillantes.
    *   Signalement des domaines frauduleux aux registrars pour suspension.
    *   Remboursement des utilisateurs affectés.
    *   Avertissement de la communauté contre les tentatives d'usurpation d'identité du support et les escroqueries.
*   **Pour les utilisateurs :**
    *   Désinstaller la version compromise de l'extension Trust Wallet et installer la dernière version disponible à partir de sources officielles et sécurisées.
    *   Être extrêmement vigilant face aux communications (e-mails, messages, publicités) prétendant venir de Trust Wallet, en particulier celles demandant des informations personnelles ou des détails de portefeuille.
    *   Utiliser des mots de passe forts et uniques pour tous les comptes.
    *   Activer l'authentification à deux facteurs lorsque cela est possible.
    *   Surveiller activement les activités de son portefeuille.
*   **Pour l'industrie (implicite par la campagne Shai-Hulud) :**
    *   Renforcer la sécurité de la chaîne d'approvisionnement logicielle, notamment pour les paquets npm.
    *   Mettre en place des mécanismes robustes pour la gestion et la protection des secrets de développeur.
    *   Surveiller et auditer régulièrement les bibliothèques et dépendances utilisées dans les projets.

---
[Source](https://www.bleepingcomputer.com/news/security/trust-wallet-links-85-million-crypto-theft-to-shai-hulud-npm-attack/){:target="_blank"}
