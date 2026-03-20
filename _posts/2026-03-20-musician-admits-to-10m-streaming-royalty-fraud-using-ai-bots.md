---
title: 'Musician admits to $10M streaming royalty fraud using AI bots'
date: 2026-03-20
permalink: /posts/2026/03/20/musician-admits-to-10m-streaming-royalty-fraud-using-ai-bots/
tags:
- veille-cyber
- bleepingcomp
---
### Fraude massive aux redevances de streaming par IA

Michael Smith, un musicien de Caroline du Nord, a plaidé coupable d'une escroquerie ayant généré plus de 10 millions de dollars de revenus illégaux sur des plateformes comme Spotify, Apple Music et Amazon Music. Entre 2017 et 2024, il a utilisé des centaines de milliers de titres générés par intelligence artificielle, diffusés des milliards de fois par un réseau de plus de 1 000 comptes automatisés (bots).

**Points clés :**
*   **Mécanisme :** Utilisation d'une infrastructure composée de 52 comptes de services cloud, chacun exploitant 20 comptes de bots, pour un volume quotidien estimé à plus de 660 000 écoutes.
*   **Contournement :** Emploi de VPN pour masquer l'origine des connexions et dilution des écoutes sur une vaste quantité de titres pour éviter les seuils d'alerte des algorithmes antifraude.
*   **Impact financier :** Le fraudeur a détourné des millions de dollars destinés aux artistes légitimes et devra verser plus de 8 millions de dollars en restitution.

**Vulnérabilités exploitées :**
*   Absence de validation stricte de l'authenticité des auditeurs par les plateformes de streaming.
*   Failles dans les systèmes de détection de comportements anormaux (le volume élevé de titres avec un faible nombre d'écoutes individuelles permettait de rester sous les radars).
*   *Note : Aucune CVE n'est applicable ici, s'agissant d'une fraude opérationnelle et non d'une exploitation de vulnérabilité logicielle spécifique.*

**Recommandations :**
*   **Détection comportementale avancée :** Renforcer les systèmes antifraude pour identifier les modèles de consommation non humains, notamment la corrélation entre les adresses IP (même via VPN) et les patterns de lecture répétitifs.
*   **Audit des métadonnées :** Implémenter des contrôles plus rigoureux sur l'origine et la qualité du contenu pour détecter les titres générés massivement par IA visant uniquement l'extraction de royalties.
*   **Analyse de risques :** Surveiller les pics de création de comptes et les taux de lecture atypiques sur les nouveaux catalogues d'artistes peu connus pour bloquer préventivement les botnets à grande échelle.

---
[Source](https://www.bleepingcomputer.com/news/security/musician-pleads-guilty-to-10m-streaming-fraud-powered-by-ai-bots/){:target="_blank"}
