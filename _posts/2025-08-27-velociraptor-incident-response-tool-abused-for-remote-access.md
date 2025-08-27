---
title: 'Velociraptor incident response tool abused for remote access'
date: 2025-08-27
permalink: /posts/2025/08/27/velociraptor-incident-response-tool-abused-for-remote-access/
tags:
- veille-cyber
- sophos
---
### L'outil d'intervention Velociraptor détourné pour un accès à distance

Des acteurs malveillants ont exploité l'outil légitime d'analyse forensique et de réponse aux incidents (DFIR) Velociraptor pour obtenir un accès à distance à des systèmes. Dans une récente intrusion, l'outil a été utilisé pour déployer Visual Studio Code (VS Code) avec l'option de tunnel activée. Cette fonctionnalité permet un accès et une exécution de code à distance, et a été précédemment abusée par plusieurs groupes de menaces.

L'attaquant a d'abord utilisé l'utilitaire Windows `msiexec` pour télécharger un installateur (`v2.msi`) depuis un domaine Cloudflare Workers (`files[.]qaubctgg[.]workers[.]dev`). Ce domaine semble servir de dépôt pour les outils de l'attaquant, incluant des utilitaires de tunneling et de contrôle à distance. L'installation de Velociraptor a été suivie par l'exécution de VS Code (`code.exe`), également téléchargé depuis ce même domaine, avec l'option de tunnel activée. L'attaquant a ensuite installé VS Code comme un service et a redirigé sa sortie vers un fichier journal. Ultérieurement, `msiexec` a été à nouveau employé pour télécharger un autre logiciel malveillant (`sc.msi`).

L'activité liée au tunneling de VS Code a déclenché une alerte qui a mené à une enquête. Les mesures correctives mises en place ont permis d'isoler l'hôte affecté, empêchant l'attaquant d'atteindre ses objectifs, qui auraient probablement conduit à un déploiement de rançongiciel.

Cette tactique représente une évolution par rapport à l'abus d'outils de surveillance et de gestion à distance (RMM) par les acteurs malveillants. Elle met en évidence une tendance où les outils DFIR sont détournés pour s'introduire dans un réseau et minimiser le déploiement de malwares distincts.

**Points clés :**

*   Abus de l'outil DFIR légitime Velociraptor.
*   Utilisation de Velociraptor pour déployer Visual Studio Code avec l'option de tunnel activée.
*   Objectif probable de créer un tunnel vers un serveur de commande et contrôle (C2).
*   Utilisation de domaines Cloudflare Workers pour héberger les outils malveillants.
*   L'activité a été détectée par une alerte de sécurité (Taegis).
*   Cette méthode permet aux attaquants d'établir un accès à distance et d'exécuter du code.
*   La menace a été stoppée avant le déploiement de rançongiciels.

**Vulnérabilités :**

*   L'article ne mentionne pas de vulnérabilités spécifiques (CVE) dans Velociraptor lui-même. L'exploitation réside dans l'abus de fonctionnalités légitimes de VS Code et dans la manière dont l'attaquant a utilisé Velociraptor pour déployer ces éléments.

**Recommandations :**

*   Surveiller et enquêter sur toute utilisation non autorisée de Velociraptor.
*   Considérer toute observation de ce type de comportement comme un précurseur potentiel de rançongiciel.
*   Mettre en œuvre un système de détection et de réponse sur point de terminaison (EDR).
*   Surveiller les outils inattendus et les comportements suspects.
*   Appliquer les meilleures pratiques de sécurisation des systèmes et de sauvegarde des données.
*   Utiliser les indicateurs de compromission fournis pour examiner et restreindre l'accès aux domaines malveillants.

**Indicateurs de compromission :**

*   **Domaines :**
    *   `files[.]qaubctgg[.]workers[.]dev` ( héberge les outils de la campagne)
    *   `velo[.]qaubctgg[.]workers[.]dev` (serveur C2 de la campagne)

**Détections Sophos :**

*   Troj/Agent-BLMR
*   Troj/BatDl-PL
*   Troj/Mdrop-KDK

---
[Source](https://news.sophos.com/en-us/2025/08/26/velociraptor-incident-response-tool-abused-for-remote-access/){:target="_blank"}
