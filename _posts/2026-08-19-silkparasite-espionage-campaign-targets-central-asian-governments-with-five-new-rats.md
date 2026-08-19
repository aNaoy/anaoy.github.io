---
title: 'SilkParasite Espionage Campaign Targets Central Asian Governments with Five New RATs'
date: 2026-08-19
permalink: /posts/2026/08/19/silkparasite-espionage-campaign-targets-central-asian-governments-with-five-new-rats/
tags:
- veille-cyber
- hackernews
---
### Campagne d'espionnage SilkParasite : Ciblage gouvernemental en Asie centrale

Une nouvelle campagne de cyberespionnage baptisée **SilkParasite** cible activement des organismes gouvernementaux en Asie centrale (Ouzbékistan, Turkménistan, Kirghizistan, Tadjikistan, Kazakhstan et Géorgie). Attribué avec une confiance modérée à des acteurs liés à la Chine, ce groupe déploie un arsenal sophistiqué utilisant des outils d'assistance IA pour rationaliser le développement de malwares professionnels.

**Points clés :**
*   **Mode opératoire :** Utilisation d'e-mails de spear-phishing contenant des archives RAR protégées par mot de passe avec des documents Microsoft Office piégés.
*   **Technique d'exécution :** Emploi systématique du *DLL sideloading* via des exécutables légitimes signés numériquement pour charger des charges utiles malveillantes.
*   **Modularité :** Les malwares utilisent une architecture en plugins, permettant une adaptation flexible à l'environnement de la victime et une discrétion accrue.
*   **Évasion :** Les scripts vérifient la présence de l'antivirus Kaspersky avant l'exécution pour éviter toute détection dans la région.
*   **Arsenal :** Déploiement de sept familles de RAT (Remote Access Tools), dont cinq inédites : **DriveSilkRAT, CookiETagRAT, NomadRAT, GoginRAT et NodeEdgeRAT**. Le groupe utilise également des versions mises à jour de **BLOODALCHEMY** et **SpiceRAT**.

**Vulnérabilités :**
*   Bien qu'aucune CVE spécifique ne soit mentionnée pour une faille logicielle précise, la campagne exploite la vulnérabilité structurelle liée au **DLL sideloading** sur les systèmes Windows. Cette technique repose sur la capacité des applications à charger des bibliothèques dynamiques (DLL) situées dans le même répertoire que l'exécutable, contournant ainsi les mécanismes de sécurité standard.

**Recommandations :**
*   **Surveillance comportementale :** Ne pas se fier uniquement aux signatures de fichiers. Mettre en place des lignes de base comportementales pour détecter les relations inhabituelles entre les processus et les services réseau (ex: une application signée chargeant une DLL depuis un emplacement non standard).
*   **Gestion des vecteurs d'attaque :** Restreindre l'exécution de macros Office et surveiller l'exécution de binaires depuis des répertoires temporaires ou inhabituels.
*   **Détection du Sideloading :** Identifier les paires suspectes composées d'un binaire légitime et d'une DLL malveillante placée à proximité.
*   **Protection des endpoints :** Maintenir les solutions de sécurité à jour et configurer des règles strictes sur le chargement des bibliothèques logicielles.

---
[Source](https://thehackernews.com/2026/08/silkparasite-espionage-campaign-targets.html){:target="_blank"}
