---
title: 'Critical cPanel Flaw Could Let One Hosting Customer Take Root Control of a Whole Server'
date: 2026-08-28
permalink: /posts/2026/08/28/critical-cpanel-flaw-could-let-one-hosting-customer-take-root-control-of-a-whole-server/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans cPanel : Risque d'élévation de privilèges root

Une faille de sécurité critique affecte les fonctionnalités de « stationnement de domaine » (domain parking) et de « domaines additionnels » au sein de cPanel et WebHost Manager (WHM). Cette vulnérabilité permet à un utilisateur authentifié disposant de ces permissions de créer des fichiers arbitraires sur le serveur, conduisant à une exécution de code avec les privilèges `root` et une prise de contrôle totale du système.

**Points clés :**
*   **Vulnérabilité :** CVE-2026-65643.
*   **Impact :** Compromission complète du serveur par un utilisateur malveillant.
*   **Versions concernées :** Toutes les versions supportées de cPanel & WHM.
*   **État de l'exploitation :** Aucune information sur une exploitation active n'a été confirmée à ce jour, et la vulnérabilité ne figure pas encore au catalogue KEV de la CISA.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs en mettant à jour cPanel vers les versions suivantes (ou supérieures) :
    *   11.110.0.141
    *   11.134.0.53
    *   11.136.0.37
    *   11.138.0.2
    *   11.138.1.7 (WP Squared)
*   **Méthodes d'installation :** 
    *   Via terminal (root) : `/scripts/upcp --force`
    *   Via l'interface WHM : *Home > cPanel > Upgrade to Latest Version*
*   **Cas des serveurs obsolètes :** Les versions en fin de vie doivent être mises à niveau vers une version supportée pour bénéficier du correctif.
*   **Vérification :** Bien que le patch sécurise le serveur pour l'avenir, il ne permet pas d'annuler une compromission antérieure. Il est conseillé de surveiller les journaux du système pour détecter toute activité suspecte.

---
[Source](https://thehackernews.com/2026/08/critical-cpanel-flaw-could-let-one.html){:target="_blank"}
