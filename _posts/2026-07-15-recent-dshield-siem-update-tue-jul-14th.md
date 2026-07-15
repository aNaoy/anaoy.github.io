---
title: 'Recent DShield SIEM Update, (Tue, Jul 14th)'
date: 2026-07-15
permalink: /posts/2026/07/15/recent-dshield-siem-update-tue-jul-14th/
tags:
- veille-cyber
- sans-isc
---
### Évolution et nouvelles fonctionnalités du DShield SIEM

La mise à jour de septembre 2025 du DShield SIEM (passant à la version ELK 8.19.15) intègre des outils avancés pour une meilleure analyse des menaces détectées par les capteurs honeypot.

**Points clés :**
*   **Collecte des journaux TTY :** Les commandes saisies par les attaquants sur les capteurs sont désormais capturées, encodées en base64, puis transmises quotidiennement au SIEM. Ces données permettent d'identifier les séquences de commandes exécutées par les acteurs malveillants.
*   **Intégration de Suricata :** Les alertes et événements générés par Suricata sont maintenant consolidés dans les tableaux de bord du SIEM.
*   **Amélioration des tableaux de bord :** Une synchronisation inter-tableaux a été ajoutée, permettant de filtrer dynamiquement les données (ex: sélectionner une adresse IP réplique la requête sur l'ensemble des vues). Une carte de menaces (Threat Map) a également été implémentée pour visualiser le trafic en temps réel.

**Vulnérabilités :**
*   Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans cette mise à jour ; il s'agit d'une évolution fonctionnelle de l'outil.

**Recommandations :**
*   **Installation des add-ons :** Pour bénéficier de la visibilité étendue, les utilisateurs doivent configurer les nouveaux scripts d'ajout pour la collecte des logs TTY et l'intégration de Suricata, disponibles sur le dépôt GitHub officiel du projet.
*   **Mise à jour :** S'assurer que le déploiement Docker utilise bien la version ELK 8.19.15 pour garantir la compatibilité avec les nouveaux tableaux de bord et les fonctionnalités de parsing.

---
[Source](https://isc.sans.edu/diary/rss/33156){:target="_blank"}
