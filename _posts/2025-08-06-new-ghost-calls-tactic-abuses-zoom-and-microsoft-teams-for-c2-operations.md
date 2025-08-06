---
title: 'New Ghost Calls tactic abuses Zoom and Microsoft Teams for C2 operations'
date: 2025-08-06
permalink: /posts/2025/08/06/new-ghost-calls-tactic-abuses-zoom-and-microsoft-teams-for-c2-operations/
tags:
- veille-cyber
- bleepingcomp
---
**Ghost Calls : Le détournement des plateformes de visioconférence pour le C2**

Une nouvelle tactique post-exploitation, baptisée "Ghost Calls", exploite les serveurs TURN utilisés par des applications de visioconférence telles que Zoom et Microsoft Teams pour créer des canaux de commande et de contrôle (C2) dissimulés. Cette méthode contourne les défenses actuelles en utilisant des identifiants légitimes, WebRTC et des outils personnalisés, sans recourir à une vulnérabilité spécifique.

**Fonctionnement :**
Ghost Calls détourne les identifiants TURN temporaires fournis aux clients Zoom ou Teams lors des réunions. Ces identifiants permettent d'établir un tunnel WebRTC entre l'attaquant et la victime, via l'infrastructure de confiance des fournisseurs de services. Le trafic malveillant est ainsi déguisé en communications de visioconférence normales, échappant aux pare-feu, proxys et inspections TLS. Le chiffrement du trafic WebRTC renforce cette dissimulation. Cette approche offre une connectivité fiable et rapide, compatible avec les protocoles UDP et TCP sur le port 443, tout en évitant de révéler l'infrastructure de l'attaquant.

**Outil associé :**
La recherche a abouti au développement de l'utilitaire open-source "TURNt". Cet outil se compose d'un contrôleur côté attaquant et d'un relais déployé sur un système compromis. TURNt permet le proxy SOCKS, le transfert de port local ou distant, l'exfiltration de données et le tunneling de trafic VNC caché.

**Points clés :**
*   Abuse des serveurs TURN de Zoom et Microsoft Teams.
*   Utilise WebRTC pour établir des tunnels C2.
*   Détourne des identifiants légitimes pour éviter la détection.
*   Permet de dissimuler le trafic C2 dans le trafic de visioconférence normal.
*   Contourne les défenses périmétriques grâce à l'utilisation d'infrastructures fiables et de trafic chiffré.
*   Facilite des opérations avancées telles que le tunneling VNC.

**Vulnérabilités :**
Aucune vulnérabilité logicielle spécifique aux applications Zoom ou Microsoft Teams n'est directement exploitée. La tactique repose sur l'abus de fonctionnalités légitimes.

**Recommandations :**
Bien que l'article ne fournisse pas de recommandations spécifiques dans cette partie, les organisations devraient envisager de renforcer la surveillance de leur trafic réseau pour détecter des comportements anormaux, même s'ils semblent provenir de sources légitimes comme les plateformes de visioconférence. Une gestion stricte des identifiants et la limitation des privilèges sur les postes compromis sont également des mesures de sécurité fondamentales.

---
[Source](https://www.bleepingcomputer.com/news/security/new-ghost-calls-tactic-abuses-zoom-and-microsoft-teams-for-c2-operations/){:target="_blank"}
