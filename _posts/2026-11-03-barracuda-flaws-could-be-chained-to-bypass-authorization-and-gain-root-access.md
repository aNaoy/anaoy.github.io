---
title: 'Barracuda Flaws Could Be Chained to Bypass Authorization and Gain Root Access'
date: 2026-11-03
permalink: /posts/2026/11/03/barracuda-flaws-could-be-chained-to-bypass-authorization-and-gain-root-access/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans les produits Barracuda : Risque d'accès root

Deux vulnérabilités critiques affectant plusieurs produits Barracuda permettent, lorsqu'elles sont combinées, de contourner l'authentification et d'obtenir un accès root complet sur les appareils ciblés. L'exploitation nécessite un accès préalable à l'interface d'administration.

**Points clés :**
*   **Impact :** Contournement de l'autorisation et exécution de commandes avec privilèges root.
*   **Condition :** L'attaque est possible si l'interface d'administration est accessible, notamment via Internet.
*   **Produits touchés :** Email Security Gateway, Load Balancer ADC, Message Archiver, WAF Control Center, Web Application Firewall et Web Security Gateway.

**Vulnérabilités identifiées :**
*   **CVE-2026-116606 (CVSS 9.3) :** Contournement de l'autorisation pré-authentification (spécifique à l'Email Security Gateway).
*   **CVE-2026-111560 (CVSS 8.6) :** Injection de commandes (impacte l'ensemble des produits listés).

**Recommandations :**
*   **Mise à jour immédiate :** Installer les dernières versions du firmware et appliquer tous les correctifs de sécurité disponibles (des mises à jour successives peuvent être nécessaires pour les systèmes obsolètes).
*   **Sécurisation des accès :** Restreindre l'accès aux interfaces d'administration aux seuls réseaux internes de confiance.
*   **Contrôle réseau :** Mettre en œuvre des mesures de contrôle d'accès réseau strictes pour limiter l'exposition des interfaces critiques.

---
[Source](https://thehackernews.com/2026/11/barracuda-flaws-could-be-chained-to.html){:target="_blank"}
