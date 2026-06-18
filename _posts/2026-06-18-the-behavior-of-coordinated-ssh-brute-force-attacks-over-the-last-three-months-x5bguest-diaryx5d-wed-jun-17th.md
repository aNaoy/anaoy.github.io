---
title: 'The Behavior of Coordinated SSH Brute Force Attacks over the last three months &#x5b;Guest Diary&#x5d;, (Wed, Jun 17th)'
date: 2026-06-18
permalink: /posts/2026/06/18/the-behavior-of-coordinated-ssh-brute-force-attacks-over-the-last-three-months-x5bguest-diaryx5d-wed-jun-17th/
tags:
- veille-cyber
- sans-isc
---
### Analyse des campagnes de brute force SSH : Corrélation entre géopolitique et activités malveillantes

Une étude basée sur un honeypot DShield a analysé plus de 20 millions de tentatives de brute force SSH sur une période de 100 jours. Les résultats démontrent une corrélation directe entre les pics d'attaques et les événements géopolitiques mondiaux (notamment le conflit Iran/Israël/États-Unis) ainsi que la publication d'avis de vulnérabilités critiques.

**Points clés :**
*   **Synchronisation des attaques :** L'utilisation de signatures HASSH identiques, de versions SSH cohérentes et de taux de balayage uniformes confirme l'usage de botnets pilotés de manière centralisée.
*   **Infrastructure :** Les attaquants exploitent massivement des services cloud et des ASNs réputés (DigitalOcean, M247) pour masquer leur origine.
*   **Adaptabilité :** Les cybercriminels ajustent leurs campagnes en temps réel pour tirer profit de l'actualité des failles de sécurité publiées par des organismes comme la CISA.

**Vulnérabilités associées :**
*   Bien que l'article traite de la méthode d'attaque (brute force), il souligne l'exploitation opportuniste de failles critiques, notamment dans les systèmes **Cisco SD-WAN** (sujet de la directive CISA 26-03) et diverses vulnérabilités affectant les systèmes **Linux**.

**Recommandations de sécurité :**
*   **Durcissement des accès :** Désactiver systématiquement la connexion pour l'utilisateur « root ».
*   **Authentification forte :** Imposer l'authentification multi-facteurs (MFA) et privilégier l'usage de clés privées SSH (rotatées et auditées).
*   **Réduction de la surface d'attaque :** Utiliser le filtrage par IP, le géobloquage et modifier les ports SSH par défaut.
*   **Détection proactive :** Centraliser les journaux dans un SIEM et déployer des règles de détection basées sur les signatures de brute force (ex: via Snort ou Suricata) pour identifier les activités suspectes (SYN floods sur le port 22).

---
[Source](https://isc.sans.edu/diary/rss/33086){:target="_blank"}
