---
title: 'Bitget Confirms Third-Party Zero-Day Behind $387.5 Million Cryptocurrency Theft'
date: 2026-10-01
permalink: /posts/2026/10/01/bitget-confirms-third-party-zero-day-behind-3875-million-cryptocurrency-theft/
tags:
- veille-cyber
- hackernews
---
### Cyberattaque majeure contre Bitget : Analyse d'une faille zero-day

La plateforme d'échange de cryptomonnaies Bitget a subi un vol de 387,5 millions de dollars suite à une intrusion sophistiquée exploitant des failles dans des produits de sécurité tiers. Les investigations, menées par SlowMist et Mandiant, ont confirmé que les attaquants ont utilisé des vulnérabilités zero-day pour compromettre des appliances de sécurité, permettant un déplacement latéral vers les systèmes de gestion de portefeuilles de l'échange.

**Points clés :**
*   **Origine de l'attaque :** Les acteurs de la menace, soupçonnés d'être liés à la Corée du Nord, ont infiltré les systèmes dès le 31 août 2026.
*   **Mode opératoire :** Utilisation de scripts cachés, injection de commandes, déploiement de web shells sur des appliances de sécurité et installation d'outils personnalisés pour contourner les contrôles de risque et valider des retraits frauduleux.
*   **Impact :** Vol massif d'actifs sur 11 blockchains différentes (dont ETH, USDT, USDC, XRP, BNB, etc.).
*   **Gestion de crise :** Suspension temporaire des retraits et gel partiel de fonds par des entités tierces (Circle, Tether, NEAR).

**Vulnérabilités :**
*   **Zero-day :** Une vulnérabilité critique a été exploitée sur une appliance de sécurité tierce, permettant la lecture de variables d'environnement (mots de passe de base de données). 
*   *Note : Aucune référence CVE spécifique n'a été publiée à ce stade, la faille étant de type zero-day dans un logiciel tiers propriétaire.*

**Recommandations de sécurité :**
*   **Audit des tiers :** Renforcer la surveillance et l'isolation des outils de sécurité tiers connectés à des environnements critiques.
*   **Segmentation réseau :** Limiter strictement les accès latéraux entre les appliances de sécurité et les serveurs de production (wallet job servers).
*   **Gestion des accès :** Appliquer une politique de moindre privilège pour les comptes de service et les identifiants d'administration sur les plateformes de gestion.
*   **Monitoring :** Détecter activement les comportements anormaux, tels que l'exécution de scripts inconnus dans des processus de service ou des tentatives d'écriture de fichiers dans des endpoints d'exécution web.

---
[Source](https://thehackernews.com/2026/10/bitget-confirms-third-party-zero-day.html){:target="_blank"}
