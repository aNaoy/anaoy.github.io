---
title: 'GhostRedirector Hacks 65 Windows Servers Using Rungan Backdoor and Gamshen IIS Module'
date: 2025-09-04
permalink: /posts/2025/09/04/ghostredirector-hacks-65-windows-servers-using-rungan-backdoor-and-gamshen-iis-module/
tags:
- veille-cyber
- hackernews
---
**GhostRedirector : une campagne d'empoisonnement de serveurs Windows**

Une campagne de cybercriminalité, baptisée GhostRedirector, a compromis au moins 65 serveurs Windows, principalement au Brésil, en Thaïlande et au Vietnam. Cette opération, active depuis août 2024, déploie une porte dérobée en C++ nommée Rungan et un module natif pour Internet Information Services (IIS) appelé Gamshen.

**Objectifs des attaquants :**

*   **Fraude SEO :** Gamshen est conçu pour manipuler les résultats des moteurs de recherche, améliorant le classement de sites web cibles. Il cible spécifiquement les robots d'exploration de Google (Googlebot), modifiant les réponses HTTP sans affecter les visiteurs ordinaires. Cette pratique peut nuire à la réputation des sites compromis en les associant à des techniques SEO douteuses.
*   **Accès persistant :** Rungan permet l'exécution de commandes sur les serveurs infectés, notamment la création d'utilisateurs, la collecte d'informations et l'ajout d'URL pour l'écoute des requêtes. D'autres outils comme GoToHTTP, BadPotato/EfsPotato et Zunput sont également déployés pour établir des connexions à distance, élever les privilèges et déployer des web shells.

**Méthodes d'attaque :**

L'accès initial aux réseaux cibles semble se faire par l'exploitation d'une vulnérabilité, potentiellement une injection SQL. PowerShell est ensuite utilisé pour télécharger des outils supplémentaires hébergés sur un serveur de staging. L'utilisation du binaire `sqlserver.exe` et de la procédure stockée `xp_cmdshell` suggère l'exploitation de fonctionnalités SQL Server pour exécuter des commandes.

**Attribution et contexte :**

Des indices tels que des chaînes de caractères en chinois dans le code source, un certificat de signature de code émis à une entreprise chinoise et l'utilisation du mot de passe "huang" suggèrent une possible affiliation à un acteur malveillant chinois. Cette méthode d'utilisation de modules IIS malveillants pour la fraude SEO a déjà été observée chez d'autres groupes, comme DragonRank.

**Points clés :**

*   **Activité observée :** Compromission de 65+ serveurs Windows.
*   **Outils principaux :** Porte dérobée Rungan, module IIS Gamshen.
*   **Méthode d'accès initiale :** Exploitation de vulnérabilité (probablement SQL injection) suivie de l'utilisation de PowerShell.
*   **Fonctionnalités de Rungan :** Création d'utilisateurs, collecte d'informations, ajout d'URL, exécution de commandes via `CreateProcessA`.
*   **Fonctionnalités de Gamshen :** Fraude SEO via manipulation des réponses HTTP pour les robots d'exploration.
*   **Autres outils déployés :** GoToHTTP, BadPotato/EfsPotato, Zunput.
*   **Secteurs ciblés :** Éducation, santé, assurance, transport, technologie, commerce de détail.
*   **Géographies principales :** Brésil, Thaïlande, Vietnam, avec des activités également observées au Pérou, aux États-Unis, au Canada, en Finlande, en Inde, aux Pays-Bas, aux Philippines et à Singapour.
*   **Attribution potentielle :** Acteur malveillant aligné sur la Chine.

**Vulnérabilités exploitées :**

*   Une vulnérabilité non spécifiée, potentiellement une injection SQL.
*   Utilisation de la procédure stockée `xp_cmdshell` de SQL Server pour l'exécution de commandes.

**Recommandations :**

Bien que l'article ne fournisse pas de recommandations spécifiques, les mesures habituelles de cybersécurité s'appliquent :

*   **Mises à jour et correctifs :** Appliquer régulièrement les correctifs de sécurité pour les systèmes d'exploitation Windows et les logiciels serveur (notamment IIS et SQL Server).
*   **Surveillance des journaux :** Surveiller activement les journaux système et applicatifs pour détecter toute activité suspecte, notamment des exécutions PowerShell inhabituelles ou des tentatives d'accès non autorisées.
*   **Sécurisation des applications web :** Mettre en œuvre des mesures de sécurité robustes pour prévenir les injections SQL et autres vulnérabilités courantes dans les applications web.
*   **Gestion des privilèges :** Appliquer le principe du moindre privilège pour limiter l'impact potentiel d'une compromission.
*   **Segmentation réseau :** Segmenter le réseau pour contenir la propagation des menaces.
*   **Protection contre les malwares :** Utiliser des solutions antivirus et de détection d'intrusion fiables et à jour.
*   **Sensibilisation :** Former les utilisateurs aux risques de sécurité et aux bonnes pratiques.

---
[Source](https://thehackernews.com/2025/09/ghostredirector-hacks-65-windows.html){:target="_blank"}
