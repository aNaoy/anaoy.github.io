---
title: 'ToddyCat’s New Hacking Tools Steal Outlook Emails and Microsoft 365 Access Tokens'
date: 2025-11-25
permalink: /posts/2025/11/25/toddycats-new-hacking-tools-steal-outlook-emails-and-microsoft-365-access-tokens/
tags:
- veille-cyber
- hackernews
---
**ToddyCat : Nouvelles Techniques pour l'Exfiltration d'Emails et le Vol d'Identifiants Microsoft 365**

Le groupe de menace ToddyCat, actif depuis 2020, a développé de nouvelles méthodes pour accéder aux données d'emails d'entreprises ciblées, principalement en Europe et en Asie. Ces attaques visent à voler des tokens d'authentification OAuth 2.0 et des emails stockés localement.

**Points Clés et Vulnérabilités :**

*   **Vol de Tokens OAuth 2.0 :** ToddyCat utilise un outil nommé TCSectorCopy pour obtenir des tokens d'accès via le navigateur de l'utilisateur. Ces tokens peuvent ensuite être utilisés hors de l'infrastructure compromise pour accéder aux emails de l'entreprise.
*   **Extraction d'Emails Outlook :** Le même outil, TCSectorCopy, est capable d'accéder aux fichiers OST (Offline Storage Table) des installations locales de Microsoft Outlook. Il contourne les restrictions en copiant les données secteur par secteur, puis utilise XstReader pour en extraire le contenu.
*   **Vol d'Identifiants et de Cookies :** Des versions antérieures des outils Samurai et TomBerBil étaient utilisées pour voler des cookies et des identifiants depuis des navigateurs web comme Google Chrome et Microsoft Edge.
*   **Variante PowerShell de TomBerBil :** Une nouvelle variante de TomBerBil, écrite en PowerShell, a été détectée entre mai et juin 2024. Elle cible les contrôleurs de domaine avec des privilèges élevés et accède aux fichiers de navigateur via des ressources réseau partagées (SMB). Elle est capable d'extraire des données de Mozilla Firefox.
*   **Contournement du chiffrement DPAPI :** Bien que les fichiers contenant les données du navigateur soient chiffrés avec DPAPI, TomBerBil est capable de capturer la clé de chiffrement nécessaire pour les déchiffrer localement, en utilisant les clés de chiffrement utilisateur, le SID et le mot de passe.
*   **Vol de Tokens d'Accès Microsoft 365 :** Pour les organisations utilisant Microsoft 365, ToddyCat emploie l'outil open-source SharpTokenFinder pour extraire des tokens d'authentification (JWT) directement de la mémoire.
*   **Utilisation de ProcDump pour le Dump Mémoire :** Lorsque les logiciels de sécurité bloquent SharpTokenFinder, ToddyCat utilise l'outil ProcDump de Sysinternals pour réaliser un dump de la mémoire du processus Outlook.
*   **Exploitation d'une Vulnérabilité ESET :** Plus tôt en avril, le groupe a été associé à l'exploitation d'une faille de sécurité dans ESET Command Line Scanner (CVE-2024-11859, score CVSS : 6.8) pour déployer un malware inconnu, TCESB.

**Recommandations :**

Bien que l'article ne détaille pas explicitement des recommandations, les méthodes employées par ToddyCat suggèrent plusieurs pistes :

*   **Surveillance des Tokens d'Authentification :** Mettre en place des mécanismes de détection et d'alerte pour la création ou l'utilisation anormale de tokens OAuth 2.0.
*   **Sécurisation des Fichiers OST :** Renforcer les contrôles d'accès aux fichiers de stockage locaux d'Outlook et surveiller les tentatives d'accès non autorisées pendant l'exécution de l'application.
*   **Protection des Contrôleurs de Domaine :** Appliquer des politiques de sécurité strictes sur les contrôleurs de domaine, limiter les accès réseau et surveiller les activités suspectes via SMB.
*   **Gestion des Identifiants et Tokens :** Mettre en œuvre des politiques de gestion des identifiants robustes et encourager l'utilisation de l'authentification multifacteur.
*   **Surveillance des Dumps Mémoire :** Détecter et alerter sur l'utilisation d'outils comme ProcDump à des fins potentiellement malveillantes.
*   **Application des Correctifs de Sécurité :** Maintenir les systèmes à jour, y compris les scanners antivirus et les systèmes d'exploitation, pour corriger les vulnérabilités connues (comme la CVE-2024-11859).

---
[Source](https://thehackernews.com/2025/11/toddycats-new-hacking-tools-steal.html){:target="_blank"}
