---
title: '3 Reasons Attackers Are Using Your Trusted Tools Against You (And Why You Don’t See It Coming)'
date: 2026-04-01
permalink: /posts/2026/04/01/3-reasons-attackers-are-using-your-trusted-tools-against-you-and-why-you-dont-see-it-coming/
tags:
- veille-cyber
- hackernews
---
### La montée en puissance des attaques « Living off the Land » (LotL)

La cybersécurité moderne fait face à un changement de paradigme : les attaquants privilégient désormais l'utilisation d'outils légitimes déjà présents dans les environnements cibles plutôt que le déploiement de malwares classiques. Cette stratégie, appelée *Living off the Land* (LotL), permet une persistance discrète et une élévation de privilèges difficile à détecter.

**Points clés :**
* **Discrétion accrue :** 84 % des attaques exploitent des outils natifs pour contourner les défenses, rendant la distinction entre usage légitime et malveillant complexe pour les équipes de sécurité.
* **Surface d'attaque étendue :** Les systèmes d'exploitation modernes incluent des centaines de binaires natifs dont 95 % des accès par les utilisateurs sont inutiles, créant des vecteurs d'attaque inutilisés mais exploitables.
* **Limites de la détection :** La surveillance classique (EDR/XDR) peine à interpréter des comportements qui semblent normaux, laissant aux attaquants une fenêtre d'action trop large avant que l'alerte ne soit levée.

**Vulnérabilités :**
L'article ne mentionne pas de CVE spécifiques, car il se concentre sur l'abus de fonctionnalités natives :
* **Outils concernés :** PowerShell, WMIC, Certutil.
* **Failles opérationnelles :** Accès non contrôlés aux outils d'administration et autorisations excessives accordées aux utilisateurs ou aux processus sur des outils possédant des capacités détournables.

**Recommandations :**
* **Visibilité proactive :** Cartographier précisément la surface d'attaque interne pour identifier quels outils sont réellement nécessaires aux opérations et restreindre l'accès à ceux qui sont superflus.
* **Réduction des droits :** Limiter les privilèges des utilisateurs et des systèmes pour restreindre l'exécution des fonctions puissantes des binaires natifs aux seuls besoins métiers.
* **Analyse comportementale :** Passer d'une détection basée sur les fichiers suspects à une analyse contextuelle fine des comportements pour repérer les anomalies dans l'utilisation des outils légitimes.

---
[Source](https://thehackernews.com/2026/04/3-reasons-attackers-are-using-your.html){:target="_blank"}
