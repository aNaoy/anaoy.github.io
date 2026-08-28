---
title: 'GiveWP WordPress donation plugin flaw lets hackers execute server commands'
date: 2026-08-28
permalink: /posts/2026/08/28/givewp-wordpress-donation-plugin-flaw-lets-hackers-execute-server-commands/
tags:
- veille-cyber
- bleepingcomp
---
### Exécution de code à distance critique dans le plugin WordPress GiveWP

Une faille de sécurité critique permet à un attaquant non authentifié d'exécuter des commandes arbitraires sur les serveurs hébergeant des sites utilisant le plugin GiveWP. Cette vulnérabilité repose sur une chaîne d'exploitation exploitant l'enregistrement d'utilisateurs non autorisé et une injection d'objets PHP.

**Points clés :**
*   **Vecteur d'attaque :** L'attaquant contourne les paramètres de WordPress pour créer un compte utilisateur, puis injecte un objet sérialisé malveillant via une procédure de don.
*   **Mécanisme :** Le serveur désérialise cet objet lors de la navigation sur le site, déclenchant l'exécution de commandes système.
*   **Conditions :** L'attaque nécessite l'utilisation d'anciens formulaires de don sans paramètres de configuration spécifiques (`formBuilderSettings`).

**Vulnérabilité :**
*   **CVE-2026-82222 :** Affecte les versions du plugin GiveWP de 4.16.6 à 4.16.7.1.

**Recommandations :**
*   **Mise à jour immédiate :** Passer impérativement à la version 4.16.7.2 ou supérieure. Cette mise à jour bloque le traitement des données sérialisées suspectes et supprime les charges utiles déjà présentes dans la base de données.
*   **Vigilance :** Bien que le correctif empêche l'exécution de code, les administrateurs doivent noter que l'action d'enregistrement utilisateur du plugin ne respecte toujours pas les paramètres globaux de WordPress et nécessite une surveillance accrue.

---
[Source](https://www.bleepingcomputer.com/news/security/givewp-wordpress-donation-plugin-flaw-lets-hackers-execute-server-commands/){:target="_blank"}
