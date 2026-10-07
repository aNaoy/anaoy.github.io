---
title: 'SonicWall warns of max severity SSRF flaw in SMA1000 gateways'
date: 2026-10-07
permalink: /posts/2026/10/07/sonicwall-warns-of-max-severity-ssrf-flaw-in-sma1000-gateways/
tags:
- veille-cyber
- bleepingcomp
---
### Correction critique pour les passerelles SonicWall SMA1000

SonicWall a publié des correctifs urgents pour pallier une vulnérabilité critique de type SSRF (Server-Side Request Forgery) affectant ses passerelles d'accès distant sécurisé de la série SMA1000. Bien qu'aucune exploitation active ne soit actuellement recensée, la criticité élevée de cette faille impose une mise à jour immédiate des systèmes exposés.

**Points clés :**
*   **Produits concernés :** Appliances SMA1000 modèles 6210, 7210 et 8200v.
*   **Portée :** La faille réside dans l'interface « Appliance WorkPlace ». Elle n'affecte ni la série SMA 100, ni les fonctionnalités SSL-VPN des pare-feu SonicWall.
*   **Contexte :** Les produits SMA1000 sont des cibles privilégiées pour les attaquants, souvent utilisés pour déployer des ransomwares via l'exploitation de failles zero-day.

**Vulnérabilité :**
*   **CVE-2026-102255 :** Faille SSRF de sévérité maximale. Elle permet à un attaquant non authentifié, via un chemin d'accès alternatif non intentionnel, de forcer l'équipement à effectuer des requêtes vers des ressources internes, facilitant ainsi des opérations non autorisées.

**Recommandations :**
*   **Appliquer les correctifs :** Déployer immédiatement les derniers hotfixes fournis par SonicWall pour sécuriser les appliances physiques et virtuelles.
*   **Surveillance :** Les administrateurs doivent s'assurer que leurs systèmes ne sont pas exposés inutilement sur Internet, alors que plus de 400 passerelles SMA1000 sont identifiées comme accessibles publiquement.

---
[Source](https://www.bleepingcomputer.com/news/security/sonicwall-warns-of-max-severity-ssrf-flaw-in-sma1000-gateways/){:target="_blank"}
