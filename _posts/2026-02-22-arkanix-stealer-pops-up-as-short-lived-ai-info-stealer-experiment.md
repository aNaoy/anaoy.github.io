---
title: 'Arkanix Stealer pops up as short-lived AI info-stealer experiment'
date: 2026-02-22
permalink: /posts/2026/02/22/arkanix-stealer-pops-up-as-short-lived-ai-info-stealer-experiment/
tags:
- veille-cyber
- bleepingcomp
---
### L'Arkanix Stealer : Un Expérimentateur d'Infostealer Aidé par l'IA

Détecté fin 2025 sur des forums du dark web, Arkanix Stealer se présente comme un logiciel malveillant d'extraction d'informations dont le développement pourrait avoir été assisté par intelligence artificielle (IA). Ce projet éphémère, destiné à générer des gains rapides, proposait un panel de fonctionnalités standards pour les cybercriminels, incluant une architecture modulaire et des techniques d'évasion. Le projet a été abruptement arrêté par son auteur, moins de deux mois après son lancement, sans préavis.

Les chercheurs de Kaspersky, qui ont analysé Arkanix Stealer, ont relevé des indices suggérant l'utilisation de modèles de langage (LLM) pour accélérer et simplifier le processus de développement.

**Points Clés :**

*   **Nature Expérimentale :** Arkanix Stealer a probablement servi de projet pilote pour tester l'impact de l'IA sur le développement de malwares et la rapidité de mise sur le marché de nouvelles fonctionnalités.
*   **Durée de Vie Courte :** L'opération a été de courte durée, rendant sa détection et son suivi plus complexes.
*   **Modèle Commercial :** Promotion via des forums de hackers avec deux versions proposées : une version basique en Python et une version "premium" en C++ utilisant VMProtect, incluant des fonctionnalités avancées.
*   **Outils Sociaux :** Un serveur Discord était utilisé pour la communication avec les utilisateurs, les mises à jour et le support. Un programme de parrainage était également en place.
*   **Objectif Financier Rapide :** La courte existence du projet suggère une recherche de gains financiers immédiats.
*   **Évaluation :** Kaspersky le décrit davantage comme un "produit logiciel public" qu'un "stealer louche".

**Vulnérabilités et Capacités d'Extraction :**

Arkanix Stealer est capable d'extraire une large gamme de données sensibles :

*   Informations système.
*   Données stockées dans les navigateurs (historique, remplissage automatique, cookies, mots de passe) pour 22 navigateurs différents.
*   Tokens OAuth2 sur les navigateurs basés sur Chromium.
*   Données de portefeuilles de cryptomonnaies.
*   Identifiants Telegram et Discord.
*   Informations d'identification pour les services VPN tels que Mullvad, NordVPN, ExpressVPN et ProtonVPN.
*   Identifiants RDP (dans la version premium).
*   Données associées à des plateformes de jeux comme Epic Games, Battle.net, Riot, Unreal Engine, Ubisoft Connect et GOG (dans la version premium).

Il peut également :

*   S'auto-propager via l'API Discord et envoyer des messages aux contacts de la victime.
*   Archiver des fichiers du système de fichiers local pour exfiltration.
*   Prendre des captures d'écran.
*   Utiliser des modules additionnels (non détaillés avec des CVE spécifiques) comme un grabber Chrome, un patcher de portefeuille pour Exodus ou Atomic, un outil HVNC, et des extracteurs pour FileZilla et Steam.
*   La version premium intègre l'outil post-exploitation ChromElevator pour contourner les protections de Google (ABE) et voler des identifiants de navigateur.
*   Inclut des protections anti-analyse (anti-sandbox, anti-debugging).

Aucune vulnérabilité spécifique (avec CVE) n'est directement attribuée à Arkanix Stealer dans l'article, mais ses fonctionnalités exploitent les informations et identifiants stockés par les systèmes et applications ciblés.

**Recommandations :**

Bien que l'article ne détaille pas de recommandations spécifiques, l'analyse suggère les bonnes pratiques générales suivantes :

*   **Surveillance des forums malveillants :** Identifier les nouvelles menaces comme Arkanix Stealer dès leur apparition.
*   **Sécurisation des identifiants :** Utiliser des mots de passe forts et uniques, l'authentification multi-facteurs lorsque possible.
*   **Mises à jour régulières :** Maintenir les systèmes d'exploitation, les navigateurs et les applications à jour pour corriger les vulnérabilités connues.
*   **Prudence avec les sources inconnues :** Éviter de télécharger des logiciels ou de cliquer sur des liens suspects provenant de sources non fiables.
*   **Utilisation de solutions de sécurité :** Déployer des logiciels antivirus et anti-malware robustes et les maintenir à jour.
*   **Sensibilisation à la cybersécurité :** Former les utilisateurs aux risques et aux tactiques couramment utilisées par les cybercriminels.

---
[Source](https://www.bleepingcomputer.com/news/security/arkanix-stealer-pops-up-as-short-lived-ai-info-stealer-experiment/){:target="_blank"}
