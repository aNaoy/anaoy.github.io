---
title: 'Chinese-Made Zbtlink Routers Ship With Backdoor That Opens Unauthenticated Root Shells'
date: 2026-08-06
permalink: /posts/2026/08/06/chinese-made-zbtlink-routers-ship-with-backdoor-that-opens-unauthenticated-root-shells/
tags:
- veille-cyber
- hackernews
---
### Backdoor critique : La menace « ENDLESSDOORS » sur les routeurs Zbtlink

Des chercheurs de VulnCheck ont découvert une porte dérobée persistante, baptisée **ENDLESSDOORS**, intégrée dans le firmware d'au moins 20 modèles de routeurs Zbtlink. Ce mécanisme, présent depuis plus de deux ans, permet un accès root non authentifié aux équipements.

**Points clés :**
*   **Fonctionnement :** L'implant utilise l'outil `rctl` pour établir des communications avec des serveurs de commande et de contrôle (C2) situés en Chine toutes les 35 secondes.
*   **Dissimulation :** Le processus se fait passer pour un thread du noyau Linux (`kworker`) afin de passer inaperçu tout en s'exécutant avec des privilèges root.
*   **Absence de sécurité :** Le protocole ne nécessite aucun handshake ni authentification. Il suffit d'intercepter la communication ou de compromettre les domaines cibles pour prendre le contrôle total du routeur.
*   **Réaction du constructeur :** Zbtlink affirme que cet outil était destiné à la maintenance après-vente et à l'assistance au débogage. Les firmwares concernés ont été temporairement retirés de leur site web pour correction.

**Vulnérabilités :**
*   Bien qu'aucune référence CVE spécifique ne soit attribuée, la faille repose sur l'exécution arbitraire de commandes root via une porte dérobée (`rctl`) non sécurisée, présente par défaut dans le système d'exploitation du routeur.

**Recommandations :**
*   **Inspection système :** Rechercher la présence de fichiers suspects : `/usr/sbin/kworker`, `/usr/lib/librctl.so`, `/etc/kworker.cfg` et `/etc/init.d/skworker`.
*   **Contrôle réseau :** Bloquer les flux sortants vers les domaines et adresses IP associés au C2 (notamment `zbtctl.epplink.net`, `online-string.com` et les adresses IP liées aux serveurs de contrôle).
*   **Mise à jour :** Surveiller les annonces de Zbtlink pour l'application des correctifs officiels dès leur publication.
*   **Segmentation :** En attendant un correctif, isoler ces équipements sur un réseau restreint sans accès direct à Internet.

---
[Source](https://thehackernews.com/2026/08/chinese-made-zbtlink-routers-ship-with.html){:target="_blank"}
