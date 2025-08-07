---
title: 'New Ghost Calls tactic abuses Zoom and Microsoft Teams for C2 operations'
date: 2025-08-07
permalink: /posts/2025/08/07/new-ghost-calls-tactic-abuses-zoom-and-microsoft-teams-for-c2-operations/
tags:
- veille-cyber
- bleepingcomp
---
## Fantômes dans la machine : Détournement des plateformes de visioconférence pour le C2

Une nouvelle méthode post-exploitation, baptisée "Ghost Calls", exploite les serveurs TURN des plateformes de visioconférence comme Zoom et Microsoft Teams pour masquer le trafic de commande et contrôle (C2). Cette technique permet de détourner le trafic à travers des infrastructures légitimes, rendant la détection difficile.

**Points Clés :**

*   **Abus d'infrastructures fiables :** La méthode utilise les serveurs TURN, conçus pour la communication en temps réel, comme relais pour le trafic C2.
*   **Dissimulation dans le trafic légitime :** Le trafic C2 est camouflé en réunions en ligne normales, rendant son identification complexe pour les défenses existantes.
*   **Contournement des mesures de sécurité :** En passant par des domaines et adresses IP utilisés légitimement par Zoom ou Teams, le trafic malveillant peut éviter les pare-feu, proxys et inspections TLS.
*   **Outil dédié :** Un utilitaire open-source nommé 'TURNt' a été développé pour faciliter la création de tunnels C2 via les serveurs TURN de ces plateformes.
*   **Fonctionnalités de tunneling :** 'TURNt' permet le proxy SOCKS, le transfert de ports local et distant, l'exfiltration de données et le tunnelage du trafic VNC (Virtual Network Computing).

**Vulnérabilités :**

Aucune vulnérabilité spécifique dans Zoom ou Microsoft Teams n'est exploitée par cette technique. L'attaque repose sur l'abus des fonctionnalités existantes des protocoles TURN et WebRTC.

**Recommandations :**

Les éditeurs de plateformes de visioconférence comme Zoom et Microsoft Teams sont contactés pour évaluer et potentiellement renforcer leurs mesures de sécurité afin de limiter la faisabilité de cette tactique.

---
[Source](https://www.bleepingcomputer.com/news/security/new-ghost-calls-tactic-abuses-zoom-and-microsoft-teams-for-c2-operations/){:target="_blank"}
