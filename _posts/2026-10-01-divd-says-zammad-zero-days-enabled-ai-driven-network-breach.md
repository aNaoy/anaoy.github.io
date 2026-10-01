---
title: 'DIVD says Zammad zero-days enabled AI-driven network breach'
date: 2026-10-01
permalink: /posts/2026/10/01/divd-says-zammad-zero-days-enabled-ai-driven-network-breach/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités exploitées dans le système Zammad par un agent IA

L'organisation néerlandaise DIVD a été victime d'une cyberattaque sophistiquée utilisant un agent d'intelligence artificielle autonome pour exploiter une chaîne de deux vulnérabilités "zero-day" au sein de la plateforme de ticketing open-source Zammad. Grâce à l'automatisation, l'attaquant a pu exécuter l'intrusion, l'élévation de privilèges et l'exfiltration de données en quelques secondes seulement.

**Points clés :**
*   **Mode opératoire :** L'attaque était entièrement pilotée par un agent IA capable de prendre des décisions autonomes sans intervention humaine.
*   **Impact :** L'intrusion a permis le détournement de session, l'exécution de code à distance (RCE) et l'élévation de privilèges jusqu'au niveau "root".
*   **Limitation :** La segmentation réseau et la réactivité de l'équipe de réponse aux incidents ont permis de contenir l'attaque et d'empêcher une propagation latérale plus profonde.
*   **Contexte :** Zammad est une solution largement utilisée par des milliers d'entreprises et organisations internationales.

**Vulnérabilités :**
*   **CVE-2026-102489**
*   **CVE-2026-102490**

**Recommandations :**
*   **Mise à jour immédiate :** Les utilisateurs de Zammad doivent impérativement migrer vers la **version 7**, considérée comme sécurisée.
*   **Mesure d'urgence :** En cas d'impossibilité de mise à jour immédiate, il est conseillé de déconnecter les instances exposées du réseau.

---
[Source](https://www.bleepingcomputer.com/news/security/divd-says-zammad-zero-days-enabled-ai-driven-network-breach/){:target="_blank"}
