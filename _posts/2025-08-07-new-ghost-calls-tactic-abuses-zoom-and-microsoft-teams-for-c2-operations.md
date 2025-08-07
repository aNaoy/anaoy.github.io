---
title: 'New Ghost Calls tactic abuses Zoom and Microsoft Teams for C2 operations'
date: 2025-08-07
permalink: /posts/2025/08/07/new-ghost-calls-tactic-abuses-zoom-and-microsoft-teams-for-c2-operations/
tags:
- veille-cyber
- bleepingcomp
---
**Le détournement des serveurs TURN pour le Command & Control**

Une nouvelle technique d'évasion des opérations de commandement et de contrôle (C2) post-exploitation, baptisée "Ghost Calls", exploite les serveurs TURN utilisés par les plateformes de visioconférence telles que Zoom et Microsoft Teams. Cette méthode permet de dissimuler le trafic malveillant en le faisant transiter par l'infrastructure légitime de ces services.

**Points clés :**

*   **Abus des serveurs TURN :** Ghost Calls détourne les identifiants temporaires des serveurs TURN, attribués lors des sessions de visioconférence, pour établir des tunnels WebRTC.
*   **Contournement des défenses :** En utilisant des identifiants légitimes, WebRTC et des outils personnalisés, cette technique évite la plupart des mesures de sécurité et anti-abus sans recourir à une vulnérabilité logicielle (exploit).
*   **Dissimulation dans le trafic légitime :** Le trafic C2 transite par des domaines et adresses IP couramment utilisés par les entreprises, le rendant difficile à distinguer du trafic normal de visioconférence.
*   **Chiffrement WebRTC :** Le trafic WebRTC étant chiffré, il est efficacement dissimulé.
*   **Avantages pour l'attaquant :** La méthode offre une connectivité performante et fiable, la possibilité d'utiliser UDP et TCP sur le port 443, et évite d'exposer l'infrastructure de l'attaquant.
*   **Outil "TURNt" :** Un utilitaire open-source, TURNt, a été développé pour faciliter le tunneling du trafic C2 via les serveurs TURN de Zoom et Teams. Il permet le proxy SOCKS, le transfert de ports, l'exfiltration de données et le tunneling VNC caché.

**Vulnérabilités :**

Aucune vulnérabilité logicielle spécifique (CVE) n'est exploitée. La technique repose sur un abus des protocoles et de l'infrastructure existants.

**Recommandations :**

Bien que l'article ne propose pas de recommandations directes, il souligne la nécessité pour les éditeurs de plateformes de visioconférence (Zoom, Microsoft Teams) d'envisager des mesures de sécurité supplémentaires pour atténuer la faisabilité de telles attaques. Pour les organisations, une vigilance accrue sur le trafic réseau et la détection des activités inhabituelles, même au sein des flux de visioconférence, pourrait être pertinente.

---
[Source](https://www.bleepingcomputer.com/news/security/new-ghost-calls-tactic-abuses-zoom-and-microsoft-teams-for-c2-operations/){:target="_blank"}
