---
title: 'American Organizations Under Attack: Skyw4lker Device Code Phishing Campaign Exposed'
date: 2026-10-28
permalink: /posts/2026/10/28/american-organizations-under-attack-skyw4lker-device-code-phishing-campaign-exposed/
tags:
- veille-cyber
- hackernews
---
### Analyse de la campagne de phishing "Skyw4lker"

La campagne « Skyw4lker » cible principalement les secteurs de la fabrication, de la technologie et de la santé aux États-Unis. Contrairement au phishing classique, elle n'exploite pas le vol direct d'identifiants, mais utilise des flux d'authentification légitimes pour détourner des jetons de session Microsoft 365.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation de documents protégés par mot de passe (présentés comme des contrats ou des propositions commerciales) qui redirigent les victimes vers des pages hébergées sur `sites[.]google[.]com`.
*   **Technique :** L'attaquant force une authentification légitime. La victime est incitée à compléter une procédure d'autorisation de périphérique, permettant à l'attaquant de récupérer des jetons d'accès valides pour Microsoft 365.
*   **Infrastructure :** Le kit de phishing repose sur du JavaScript obfusqué et un backend PHP pour capturer les métadonnées (IP, géolocalisation) et maintenir une session active avec la victime.
*   **Difficulté de détection :** L'authentification apparaissant comme légitime dans les journaux système, elle échappe souvent aux outils de surveillance basés uniquement sur les anomalies d'identité.

**Vulnérabilités :**
*   Cette attaque n'exploite pas une faille logicielle spécifique (CVE), mais la confiance accordée aux flux d'authentification légitimes et le manque de visibilité comportementale sur les processus d'autorisation de périphériques.

**Recommandations :**
*   **Analyse comportementale :** Privilégier l'utilisation de "sandboxes" interactives pour observer le comportement réel des documents suspects, au-delà de leur simple signature statique.
*   **Corrélation des logs :** Ne pas se contenter de surveiller les succès d'authentification ; corréler les accès avec l'activité réseau, les redirections web et le contexte du terminal utilisé.
*   **Automatisation du renseignement :** Intégrer des flux de renseignements sur les menaces (Threat Intel) dans les systèmes de détection (SIEM/XDR) pour identifier les domaines et IP malveillants connus dès la tentative d'accès.
*   **Gestion des jetons :** Renforcer les politiques de sécurité autour de l'octroi des jetons OAuth et de l'autorisation de périphériques pour limiter l'impact en cas de compromission.

---
[Source](https://thehackernews.com/2026/10/american-organizations-under-attack.html){:target="_blank"}
