---
title: 'New Ghost Calls tactic abuses Zoom and Microsoft Teams for C2 operations'
date: 2025-08-07
permalink: /posts/2025/08/07/new-ghost-calls-tactic-abuses-zoom-and-microsoft-teams-for-c2-operations/
tags:
- veille-cyber
- bleepingcomp
---
### Contournement des Défenses : La Tactique "Ghost Calls"

Une nouvelle méthode d'évasion post-exploitation, nommée "Ghost Calls", exploite les serveurs TURN des plateformes de visioconférence comme Zoom et Microsoft Teams. Elle permet aux attaquants de tunneler du trafic via l'infrastructure de ces services de confiance.

Cette technique utilise des identifiants légitimes, WebRTC et des outils personnalisés pour contourner la plupart des défenses existantes, sans nécessiter d'exploit. Elle permet aux opérateurs de dissimuler des sessions de commande et contrôle (C2) dans le trafic normal des réunions en ligne.

**Fonctionnement :**
Les serveurs TURN (Traversal Using Relays around NAT) aident les applications comme Zoom et Teams à établir des communications lorsque les connexions directes ne sont pas possibles. "Ghost Calls" détourne les identifiants TURN temporaires attribués aux clients pour créer un tunnel WebRTC entre l'attaquant et la victime. Ce tunnel permet de masquer le trafic C2 comme du trafic de visioconférence légitime, traversant ainsi les pare-feux et autres inspections de sécurité. Le trafic WebRTC étant chiffré, il est difficile à détecter. Cette approche offre une connectivité performante et fiable, utilisant le protocole UDP et TCP sur le port 443.

**Outil :**
Le chercheur Adam Crosser a développé "TURNt", un utilitaire open-source pour réaliser ce type de tunneling. Il comprend un contrôleur côté attaquant et un relais déployé sur une machine compromise. TURNt peut effectuer du proxy SOCKS, du transfert de port local ou distant, de l'exfiltration de données et du tunneling VNC caché.

**Points Clés :**

*   Utilise les serveurs TURN de Zoom et Teams pour le C2.
*   Contourne les défenses sans exploit.
*   Dissimule le trafic C2 dans le trafic de visioconférence légitime.
*   Offre une connectivité performante et chiffrée.
*   L'outil "TURNt" facilite le proxy, le transfert de port et le tunneling VNC.

**Vulnérabilités :**
Aucune vulnérabilité spécifique aux applications Zoom ou Microsoft Teams n'est exploitée. La méthode abuse de la fonctionnalité légitime des serveurs TURN.

**Recommandations :**
Il est conseillé aux entreprises de surveiller activement le trafic réseau pour identifier les comportements anormaux, même s'ils transitent par des canaux apparemment légitimes. Des mesures visant à restreindre l'utilisation des serveurs TURN à des fins non prévues ou à mettre en place des mécanismes d'authentification plus robustes pour ces serveurs pourraient être envisagées par les fournisseurs de services.

---
[Source](https://www.bleepingcomputer.com/news/security/new-ghost-calls-tactic-abuses-zoom-and-microsoft-teams-for-c2-operations/){:target="_blank"}
