---
title: 'ToddyCat: your hidden email assistant. Part 2'
date: 2026-06-30
permalink: /posts/2026/06/30/toddycat-your-hidden-email-assistant-part-2/
tags:
- veille-cyber
- securelist
---
### L'outil Umbrij : Automatisation du vol de jetons OAuth par ToddyCat

Le groupe APT ToddyCat a développé un nouvel outil malveillant nommé **Umbrij**, conçu pour automatiser l'exfiltration de données depuis des comptes Gmail professionnels. En exploitant des sessions actives dans des navigateurs basés sur Chromium, les attaquants détournent le protocole OAuth 2.0 pour obtenir des jetons d'accès via l'API Google, leur permettant ainsi d'accéder aux emails des victimes sans déclencher d'alertes de sécurité classiques.

#### Points clés de l'attaque
*   **Technique d'exécution :** Utilisation du **DLL sideloading** pour charger Umbrij via des exécutables légitimes (Bitdefender ConnectAgent, Visual Studio, Google Desktop Search).
*   **Shadow Token via Remote Debug (STRD) :** Umbrij lance le navigateur en mode "headless" (sans interface) sur un port de débogage distant. Il copie le profil utilisateur local pour réutiliser une session authentifiée, simule des clics via JavaScript pour valider les permissions d'accès, et extrait le code d'autorisation OAuth.
*   **Automatisation :** Le processus est entièrement automatisé, de l'extraction des cookies à la récupération du jeton d'accès, avec une journalisation détaillée pour les opérateurs.

#### Vulnérabilités exploitées
Bien qu'il n'y ait pas de CVE spécifique, l'attaque repose sur :
*   **DLL Sideloading :** Exploitation du chargement non sécurisé de bibliothèques par des exécutables signés.
*   **Abus de fonctionnalités légitimes :** Utilisation détournée des options de débogage distant (--remote-debugging-port) des navigateurs.
*   **Persistance de session :** Exploitation de sessions Google actives sur les postes de travail.

#### Recommandations de sécurité
*   **Surveillance des logs :** Détecter le chargement de DLL suspectes par des applications légitimes et surveiller les lancements de navigateurs avec des arguments `--remote-debugging-port`.
*   **Durcissement (Hardening) :** Désactiver les outils de développement dans les navigateurs via la stratégie de groupe (GPO) `DeveloperToolsAvailability` (valeur `0x00000002`).
*   **Audit OAuth :** Vérifier les applications tierces autorisées sur les comptes Google Workspace via la console d'administration. Révoquer tout accès non reconnu, en particulier pour *Google Workspace Migration/Sync for Microsoft Outlook* si ces outils ne sont pas utilisés.
*   **Bonnes pratiques utilisateurs :** Sensibiliser à la déconnexion systématique des sessions Google sur les postes de travail en fin de session.

---
[Source](https://securelist.com/toddycat-apt-umbrij-tool-and-oauth/120251/){:target="_blank"}
