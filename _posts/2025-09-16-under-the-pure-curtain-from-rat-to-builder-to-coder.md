---
title: 'Under the Pure Curtain: From RAT to Builder to Coder'
date: 2025-09-16
permalink: /posts/2025/09/16/under-the-pure-curtain-from-rat-to-builder-to-coder/
tags:
- veille-cyber
- zerodaysfans
---
## L'Écosystème Logiciel Malveillant Pure : Une Analyse Approfondie

Une campagne de phishing "ClickFix" a réussi à s'introduire dans un système pendant huit jours, déployant une chaîne d'outils malveillants incluant un chargeur Rust, le RAT PureHVNC et le framework de commande et contrôle Sliver. Cette analyse détaillée se penche sur le RAT PureHVNC, ses commandes et plugins, ainsi que sur l'infrastructure de son développeur, connu sous le nom de "PureCoder".

**Points Clés :**

*   **Campagne "ClickFix" :** Utilisation d'offres d'emploi frauduleuses pour inciter les victimes à exécuter un script malveillant via la technique "ClickFix".
*   **PureHVNC RAT :** Analyse approfondie de ce RAT, y compris sa gamme complète de commandes et de plugins.
*   **Infrastructure du Développeur :** Identification de liens directs entre les serveurs de commande et contrôle du RAT et des comptes GitHub appartenant à PureCoder, le développeur de la famille de malwares Pure.
*   **Informations sur PureCoder :** Découverte du fuseau horaire d'opération (UTC+0300) et potentiels pays de résidence du développeur.
*   **PureRAT Builder :** Mise au jour d'un outil de construction pour le RAT Pure, révélant des caractéristiques liées à PureCrypter, un autre produit de PureCoder.

**Vulnérabilités et Outils :**

L'article ne détaille pas de vulnérabilités spécifiques avec des identifiants CVE. Cependant, il met en évidence l'utilisation des outils suivants par les attaquants :

*   **Rust Loader :** Chargeur malveillant développé en Rust.
*   **PureHVNC RAT :** Cheval de Troie d'accès à distance avec des capacités Hidden Virtual Network Computing (HVNC).
*   **Sliver C2 :** Framework de commande et contrôle utilisé pour la communication avec les systèmes compromis.
*   **PureCrypter :** Obfusqueur de malware.
*   **PureLogs :** Vol d'informations (stealer/logger).
*   **PureRAT Builder :** Outil permettant de générer et de configurer le RAT Pure.

**Recommandations :**

Bien que l'article se concentre sur l'analyse technique, les protections mentionnées par Check Point Research suggèrent les mesures suivantes pour se défendre contre ces menaces :

*   **Solutions de sécurité avancées :** Utilisation de technologies comme Check Point Threat Emulation et Harmony Endpoint pour une couverture complète des tactiques d'attaque, des types de fichiers et des systèmes d'exploitation.
*   **Sensibilisation aux menaces :** Informer les utilisateurs sur les techniques de phishing, telles que ClickFix et les fausses offres d'emploi.
*   **Surveillance des réseaux :** Mettre en place une surveillance pour détecter les communications avec les serveurs de commande et contrôle identifiés.
*   **Analyse des artefacts :** Examiner les fichiers suspects, notamment les scripts JavaScript et les exécutables, à la recherche d'indicateurs de compromission.

---
[Source](https://research.checkpoint.com/2025/under-the-pure-curtain-from-rat-to-builder-to-coder/){:target="_blank"}
