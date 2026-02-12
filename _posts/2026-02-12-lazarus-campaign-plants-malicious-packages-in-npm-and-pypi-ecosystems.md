---
title: 'Lazarus Campaign Plants Malicious Packages in npm and PyPI Ecosystems'
date: 2026-02-12
permalink: /posts/2026/02/12/lazarus-campaign-plants-malicious-packages-in-npm-and-pypi-ecosystems/
tags:
- veille-cyber
- hackernews
---
### Campagne Sophistiquée de Compromission des Répertoires de Paquets Open Source

Une campagne d'envergure, orchestrée par le groupe Lazarus lié à la Corée du Nord, cible les écosystèmes npm et PyPI via la publication de paquets malveillants. Ces attaques s'appuient sur des techniques d'ingénierie sociale avancées, notamment des campagnes de recrutement fictives axées sur la blockchain et les cryptomonnaies.

**Points Clés :**

*   **Méthodologie :** Des recruteurs fictifs contactent les développeurs sur des plateformes professionnelles comme LinkedIn, ou via des annonces sur Reddit, les incitant à exécuter des projets de démonstration. Ces projets, hébergés sur GitHub, servent de prétexte pour introduire des dépendances malveillantes via les registres npm et PyPI.
*   **Outils :** Les paquets compromis agissent comme vecteurs pour déployer un cheval de Troie d'accès à distance (RAT). Ce dernier peut collecter des informations système, énumérer des fichiers, lister des processus, manipuler des fichiers et communiquer avec un serveur de commande et contrôle (C2) sécurisé par un système de jetons.
*   **Découvertes Connexes :**
    *   Un paquet npm malveillant, "duer-js", a été découvert contenant le Bada Stealer, capable de voler des tokens Discord, des mots de passe, des cookies et des données de portefeuille de cryptomonnaies, exfiltrant ces informations vers un webhook Discord et un service de stockage de fichiers.
    *   Une autre campagne, baptisée XPACK ATTACK, exploite le code d'état HTTP 402 ("Paiement Requis") pour bloquer l'installation de paquets jusqu'à ce qu'une rançon en cryptomonnaie soit payée, tout en collectant des informations sur l'utilisateur et son système.

**Vulnérabilités et Risques :**

*   **Exploitation de la Confiance :** Le recours à des entreprises fictives et à des processus de recrutement légitimes vise à établir une fausse confiance et à inciter les développeurs à exécuter du code non vérifié.
*   **Compromission de Dépendances :** L'injection de code malveillant dans des paquets open source couramment utilisés permet une diffusion potentiellement large des infections.
*   **Vol de Données Sensibles :** Les RAT et les stealers sont conçus pour exfiltrer des informations critiques, y compris des identifiants, des données financières et des informations sur les systèmes.
*   **Ransomware via l'Installation :** La tactique du code HTTP 402 transforme le processus d'installation en une forme de ransomware.

**Recommandations :**

*   **Vérification Rigoureuse des Dépendances :** Examiner attentivement les nouvelles dépendances et les mises à jour de paquets avant de les intégrer dans les projets. Utiliser des outils d'analyse de sécurité pour détecter les paquets potentiellement malveillants.
*   **Prudence avec les Offres d'Emploi Inattendues :** Se méfier des offres d'emploi provenant de sources non vérifiées, en particulier celles qui demandent l'exécution de code ou de projets techniques dans le cadre du processus de candidature.
*   **Maintien des Systèmes à Jour :** S'assurer que les environnements de développement et les systèmes d'exploitation sont correctement patchés pour réduire la surface d'attaque.
*   **Segmentation et Isolation :** Si possible, exécuter des tests de paquets dans des environnements isolés (sandbox) avant de les déployer en production.
*   **Surveillance des Communications C2 :** Mettre en place des mécanismes de surveillance réseau pour détecter les communications suspectes avec des serveurs de commande et contrôle inconnus.

---
[Source](https://thehackernews.com/2026/02/lazarus-campaign-plants-malicious.html){:target="_blank"}
