---
title: 'Attackers Abuse MSP360 to Deploy ScreenConnect in Dual-RMM Phishing Attacks'
date: 2026-09-30
permalink: /posts/2026/09/30/attackers-abuse-msp360-to-deploy-screenconnect-in-dual-rmm-phishing-attacks/
tags:
- veille-cyber
- hackernews
---
### Abus des outils RMM pour des intrusions persistantes par phishing

Des campagnes de phishing observées depuis juillet 2026 exploitent des logiciels légitimes de gestion à distance (RMM) pour compromettre des systèmes Windows. Les attaquants utilisent des noms de fichiers trompeurs (invitations, mises à jour, documents administratifs) pour inciter les victimes à exécuter un installateur MSP360 légitime, mais malveillant.

**Points clés :**
*   **Stratégie "Double RMM" :** L'installation de MSP360 sert de vecteur initial, permettant ensuite de déployer secrètement *ConnectWise ScreenConnect* pour établir un canal d'accès distant redondant.
*   **Persistance et camouflage :** L'attaquant élève ses privilèges via l'UAC, enregistre des services Windows, crée des entrées de registre autorun et modifie les règles du pare-feu pour autoriser le trafic sur le port 48678.
*   **Diversification :** Des tactiques similaires ont été observées en remplaçant MSP360 par *Faronics Deploy Agent*, confirmant une méthodologie consistant à détourner divers outils d'administration légitimes pour éviter la détection.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur l'abus de fonctionnalités légitimes de logiciels d'administration (Living-off-the-land). La compromission est facilitée par l'ingénierie sociale et l'utilisation de privilèges élevés via l'UAC.

**Recommandations :**
*   **Filtrage des emails :** Renforcer la vigilance sur les emails contenant des fichiers exécutables (.exe) ou des liens de téléchargement provenant de services cloud publics (S3, Dropbox, GitLab, etc.).
*   **Surveillance des outils RMM :** Auditer strictement l'utilisation des outils de gestion à distance. Bloquer ou restreindre l'installation de logiciels RMM non approuvés par le service informatique.
*   **Contrôle des privilèges :** Limiter les droits d'administration locale des utilisateurs pour empêcher l'exécution silencieuse d'installateurs nécessitant une élévation de privilèges UAC.
*   **Analyse comportementale :** Surveiller la création inhabituelle de services Windows, les modifications du pare-feu et l'exécution de commandes PowerShell initiées par des agents RMM.

---
[Source](https://thehackernews.com/2026/09/attackers-abuse-msp360-to-deploy.html){:target="_blank"}
