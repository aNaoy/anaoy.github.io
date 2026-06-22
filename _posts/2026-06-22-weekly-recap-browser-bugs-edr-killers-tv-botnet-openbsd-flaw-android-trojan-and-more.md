---
title: '⚡ Weekly Recap: Browser Bugs, EDR Killers, TV Botnet, OpenBSD Flaw, Android Trojan, and More'
date: 2026-06-22
permalink: /posts/2026/06/22/weekly-recap-browser-bugs-edr-killers-tv-botnet-openbsd-flaw-android-trojan-and-more/
tags:
- veille-cyber
- hackernews
---
# Panorama Hebdomadaire des Menaces Cyber

La semaine a été marquée par une recrudescence d'attaques exploitant des vecteurs classiques mais efficaces : compromissions d'identifiants, vulnérabilités de plugins WordPress et abus d'outils d'intégration.

### Points clés
*   **Campagne FortiBleed :** Plus de 80 000 appareils Fortinet ciblés via des attaques par force brute et réutilisation d'identifiants.
*   **EDR Killers :** Le groupe de ransomware "The Gentlemen" déploie *GentleKiller*, un framework capable de neutraliser plus de 400 processus de sécurité (CrowdStrike, Defender, SentinelOne, etc.).
*   **Infrastructures malveillantes :** L'opération internationale *Endgame* a permis de démanteler des serveurs liés à SocGholish et de nettoyer près de 15 000 sites WordPress infectés.
*   **Botnets IoT :** Le réseau *Popa* transforme des box Android TV en nœuds de sortie pour des proxys résidentiels, utilisés dans des campagnes de fraude publicitaire.
*   **Malwares mobiles :** Le troyen bancaire *Rokarolla* cible Android en se faisant passer pour des applications populaires (TikTok, Chrome) pour voler des données bancaires et surveiller les écrans via les services d'accessibilité.

### Vulnérabilités majeures
*   **CVE-2026-20253 (Splunk Enterprise) :** Critique, permet des opérations sur les fichiers sans authentification et l'exécution de code à distance (RCE).
*   **Usbliter8 :** Faille matérielle "inpatchable" dans le contrôleur USB des puces Apple A12 et A13 (nécessite un accès physique).
*   **OpenBSD PPP :** Faille d'authentification vieille de 27 ans permettant de contourner le protocole PAP.
*   **Extensions Chrome (SiderAI/MaxAI) :** Vulnérabilités critiques permettant le vol de captures d'écran et l'exécution de code arbitraire.

### Recommandations de sécurité
1.  **Hygiène des accès :** Imposer l'authentification multifacteur (MFA) sur tous les équipements exposés, notamment les pare-feu et VPN.
2.  **Gestion des vulnérabilités :** Appliquer en priorité les correctifs pour les CVE listées, en ciblant d'abord les produits réseaux (Cisco, Fortinet) et les serveurs d'entreprise (Splunk, Atlassian).
3.  **Audit des extensions :** Désinstaller les extensions de navigateur suspectes ou non indispensables (notamment SiderAI et MaxAI).
4.  **Sécurité WordPress :** Mettre à jour les CMS et plugins, supprimer les comptes inactifs et auditer les plugins "must-use" souvent détournés par les attaquants.
5.  **Monitoring SQL Server :** Surveiller l'usage des fonctionnalités d'IA natives (ex: `sp_invoke_external_rest_endpoint`) qui peuvent être détournées pour l'exfiltration de données.

---
[Source](https://thehackernews.com/2026/06/weekly-recap-browser-bugs-edr-killers.html){:target="_blank"}
