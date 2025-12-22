---
title: 'Malicious npm package steals WhatsApp accounts and messages'
date: 2025-12-22
permalink: /posts/2025/12/22/malicious-npm-package-steals-whatsapp-accounts-and-messages/
tags:
- veille-cyber
- bleepingcomp
---
**Alarme sur le registre npm : un paquet malveillant vole des identifiants WhatsApp**

Un composant du registre Node Package Manager (npm) nommé "lotusbail", qui se présentait comme une bibliothèque légitime pour l'API WhatsApp Web, a été utilisé pour voler des messages, des contacts et des identifiants de compte WhatsApp. Détecté par la société de sécurité Koi Security, ce paquet a été téléchargé plus de 56 000 fois au cours des six derniers mois.

Le mécanisme malveillant consiste en un "wrapper" qui intercepte le trafic de communication WebSocket avec WhatsApp. Il capture les jetons d'authentification et les clés de session lors de la connexion, enregistre les messages envoyés et reçus, et exfiltre la liste de contacts ainsi que les fichiers multimédias. Les données volées sont ensuite chiffrées et obfusquées avant d'être envoyées à l'attaquant.

De plus, le paquet contient du code permettant d'associer de manière persistante le compte WhatsApp de la victime à l'appareil de l'attaquant via le processus de jumelage, offrant un accès continu jusqu'à ce que la victime supprime manuellement les appareils liés. La complexité du code, incluant des pièges à boucle infinie pour rendre l'analyse difficile, a contribué à sa discrétion.

**Points Clés:**

*   **Nature de la menace:** Package npm malveillant se faisant passer pour une bibliothèque WhatsApp légitime.
*   **Fonctionnalités malveillantes:** Vol de jetons d'authentification, interception de messages, exfiltration de contacts et de fichiers, établissement d'un accès persistant au compte.
*   **Mécanisme:** Wrapper de la communication WebSocket interceptant les données avant qu'elles n'atteignent l'application de l'utilisateur.
*   **Obfuscation:** Utilisation de chiffrement RSA personnalisé, de compression LZString et de chiffrement AES pour dissimuler les données volées.
*   **Persistance:** Exploitation du jumelage d'appareils pour maintenir l'accès même après suppression du paquet.
*   **Difficulté de détection:** Utilisation de techniques d'obfuscation et de pièges à boucle pour rendre l'analyse statique compliquée.

**Vulnérabilités:**

*   Aucune CVE spécifique n'est mentionnée dans l'article pour cette menace particulière. La vulnérabilité réside dans l'acceptation et l'utilisation de paquets npm non vérifiés provenant de registres publics.

**Recommandations:**

*   **Retirer immédiatement** le paquet "lotusbail" des systèmes concernés.
*   **Vérifier les appareils liés** dans les paramètres de compte WhatsApp pour identifier et supprimer tout appareil suspect.
*   **Surveiller le comportement d'exécution** des nouvelles dépendances, en particulier les connexions sortantes inattendues lors des flux d'authentification.
*   Ne pas se fier uniquement à l'analyse du code source pour valider la sécurité d'une dépendance ; une validation du comportement réel est essentielle.

---
[Source](https://www.bleepingcomputer.com/news/security/malicious-npm-package-steals-whatsapp-accounts-and-messages/){:target="_blank"}
