---
title: 'Steam forum ClickFix attacks infect gamers with XMRig cryptominers'
date: 2026-07-26
permalink: /posts/2026/07/26/steam-forum-clickfix-attacks-infect-gamers-with-xmrig-cryptominers/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne de malwares « ClickFix » sur les forums Steam

Des acteurs malveillants exploitent les forums de discussion de Steam via des attaques de type « ClickFix ». Ils répondent aux utilisateurs rencontrant des problèmes techniques en leur suggérant d'exécuter des commandes PowerShell frauduleuses, présentées comme des correctifs de dépannage, pour infecter leur système avec le logiciel de minage XMRig.

**Points clés :**
*   **Ingénierie sociale :** Les attaquants se font passer pour des utilisateurs serviables, exploitant la confiance de la communauté pour inciter les victimes à lancer manuellement des scripts malveillants.
*   **Contournement de sécurité :** En demandant à l'utilisateur d'exécuter la commande avec des privilèges d'administrateur, les attaquants contournent certaines protections automatiques.
*   **Processus malveillant :** Le script affiche de fausses barres de progression d'optimisation Windows pour crédibiliser l'opération, tout en configurant silencieusement une persistance (tâche planifiée) et en ajoutant des exclusions dans Microsoft Defender pour éviter la détection du mineur XMRig.

**Vulnérabilités :**
*   Cette attaque ne repose pas sur une faille logicielle spécifique (CVE), mais sur **l'abus de confiance et l'exécution de code par l'utilisateur (Human-in-the-loop)**. Elle tire parti de l'exécution aveugle de scripts PowerShell non vérifiés par des utilisateurs disposant de privilèges élevés.

**Recommandations :**
*   **Prudence :** Ne jamais exécuter de commandes PowerShell ou de scripts provenant d'inconnus sur des forums, même s'ils semblent apporter une solution à un problème technique.
*   **Vérification de compromission :** Rechercher la présence du dossier `C:\Windows\Background`, d'une exclusion suspecte dans Microsoft Defender pour ce chemin, ou d'une tâche planifiée nommée `XMRig-[nom de l'ordinateur]`.
*   **Remédiation :** En cas d'infection, effectuer un scan complet avec un antivirus. Si le doute persiste, la suppression manuelle des composants (tâche, dossier, exclusion) est nécessaire, voire une réinstallation complète du système d'exploitation par mesure de sécurité.

---
[Source](https://www.bleepingcomputer.com/news/security/steam-forum-clickfix-attacks-infect-gamers-with-xmrig-cryptominers/){:target="_blank"}
