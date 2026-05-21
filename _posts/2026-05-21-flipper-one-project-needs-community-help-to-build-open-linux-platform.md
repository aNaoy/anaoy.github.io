---
title: 'Flipper One project needs community help to build open Linux platform'
date: 2026-05-21
permalink: /posts/2026/05/21/flipper-one-project-needs-community-help-to-build-open-linux-platform/
tags:
- veille-cyber
- bleepingcomp
---
### Flipper One : Un nouveau projet de plateforme Linux ouverte

Flipper Devices lance le développement du « Flipper One », une plateforme informatique portable sous Linux, distincte du célèbre Flipper Zero. Conçu comme un outil de haute performance pour l'expérimentation réseau et matérielle, ce projet vise à supporter nativement le SDR (Radio logicielle) et l'exécution locale de modèles d'IA (LLM).

**Points clés :**
*   **Architecture hybride :** Utilisation d'un SoC ARM Rockchip RK3576 (8 Go de RAM) pour le système Linux et d'un microcontrôleur Raspberry Pi RP2350 pour la gestion indépendante du matériel (écran, alimentation, boot).
*   **Modularité poussée :** Support d'interfaces variées (M.2, GPIO, PCIe, USB 3.1, SATA) permettant l'ajout de modules Wi-Fi, de stockage SSD, d'accélérateurs IA ou de modems satellites/5G.
*   **Objectifs polyvalents :** Le dispositif est pensé pour servir de routeur, passerelle VPN, station de travail Linux portable ou centre multimédia.
*   **Défis techniques :** Le projet cherche à intégrer le support mainline du SoC dans le noyau Linux pour s'affranchir des blobs propriétaires et des dépendances spécifiques aux fabricants de puces.

**Vulnérabilités et risques :**
*   L'article ne mentionne aucune CVE spécifique, le produit étant encore à l'état de prototype en phase de développement.
*   Risques inhérents : Incertitudes liées à la chaîne d'approvisionnement (crise des puces RAM), complexité de l'architecture dual-processeur et instabilité logicielle actuelle des pilotes pour le RK3576.

**Recommandations :**
*   **Participation communautaire :** Flipper Devices invite ingénieurs et développeurs à contribuer au projet, notamment sur l'upstream du noyau Linux, le développement du firmware MCU, et la création de l'interface utilisateur "FlipCTL".
*   **Suivi du développement :** Étant donné le stade précoce du projet, il est conseillé de surveiller les annonces officielles via le profil de R&D de l'entreprise pour suivre les avancées de la mainline Linux et les résolutions des problèmes de compatibilité matérielle.

---
[Source](https://www.bleepingcomputer.com/news/hardware/flipper-one-project-needs-community-help-to-build-open-linux-platform/){:target="_blank"}
