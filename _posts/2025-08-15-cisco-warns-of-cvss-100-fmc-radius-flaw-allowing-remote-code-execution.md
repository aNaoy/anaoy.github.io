---
title: 'Cisco Warns of CVSS 10.0 FMC RADIUS Flaw Allowing Remote Code Execution'
date: 2025-08-15
permalink: /posts/2025/08/15/cisco-warns-of-cvss-100-fmc-radius-flaw-allowing-remote-code-execution/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité Critique d'Exécution de Code à Distance dans Cisco Secure FMC

Une faille de sécurité de gravité maximale (CVSS 10.0) a été identifiée dans le sous-système RADIUS du logiciel Cisco Secure Firewall Management Center (FMC). Elle permet à un attaquant non authentifié d'exécuter des commandes arbitraires avec des privilèges élevés sur les systèmes affectés.

**Points Clés et Vulnérabilités :**

*   **CVE-2025-20265 (CVSS 10.0):** Vulnérabilité dans l'implémentation RADIUS du Cisco Secure FMC Software. Un attaquant peut injecter des commandes shell arbitraires en envoyant des entrées spécialement conçues lors de l'authentification, en raison d'une gestion inadéquate des entrées utilisateur. L'exploitation nécessite que le logiciel soit configuré pour l'authentification RADIUS via l'interface web ou SSH.
*   Les versions affectées sont Cisco Secure FMC Software 7.0.7 et 7.7.0, lorsque l'authentification RADIUS est activée.
*   D'autres vulnérabilités de gravité élevée ont également été corrigées, notamment des problèmes de déni de service (DoS) dans diverses fonctions de Cisco Secure Firewall et Cisco IOS (voir la liste complète dans les références externes).

**Recommandations :**

*   Appliquer les mises à jour de sécurité fournies par Cisco pour corriger la vulnérabilité CVE-2025-20265 et les autres failles mentionnées.
*   Il n'existe pas de contournement disponible en dehors de l'application des correctifs.
*   Il est conseillé aux utilisateurs de mettre à jour leurs instances rapidement, même si aucune exploitation active n'a été signalée à ce jour.

---
[Source](https://thehackernews.com/2025/08/cisco-warns-of-cvss-100-fmc-radius-flaw.html){:target="_blank"}
