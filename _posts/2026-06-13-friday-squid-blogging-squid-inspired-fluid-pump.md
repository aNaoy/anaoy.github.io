---
title: 'Friday Squid Blogging: Squid-Inspired Fluid Pump'
date: 2026-06-13
permalink: /posts/2026/06/13/friday-squid-blogging-squid-inspired-fluid-pump/
tags:
- veille-cyber
- schneier
---
### Campagne "Atomic Arch" : compromission massive du dépôt AUR

La campagne malveillante nommée "Atomic Arch" a ciblé l'Arch User Repository (AUR), une plateforme de paquets maintenus par la communauté Arch Linux. Des attaquants ont compromis plus de 900 paquets en prenant le contrôle de comptes de développeurs ayant abandonné leurs projets (orphelins).

**Points clés :**
*   **Vecteur d'attaque :** Prise de contrôle de paquets AUR orphelins par l'utilisateur "arojas" pour y injecter du code malveillant.
*   **Sophistication :** La charge utile dépasse les standards habituels des attaques de type "drive-by" par dépôt, intégrant des techniques avancées.
*   **Envergure :** Il s'agit de l'un des incidents de chaîne d'approvisionnement (supply chain) les plus importants enregistrés pour cette plateforme.

**Vulnérabilités :**
*   L'attaque déploie un **infostealer** (logiciel de vol d'informations) ciblant spécifiquement les développeurs.
*   Installation d'un **rootkit eBPF** (Berkeley Packet Filter), permettant une persistance profonde et une exécution de code avec des privilèges élevés au niveau du noyau, rendant la détection extrêmement complexe.

**Recommandations :**
*   **Audit immédiat :** Les utilisateurs ayant installé des paquets via AUR récemment doivent vérifier leurs systèmes pour détecter toute activité inhabituelle.
*   **Sécurisation des comptes :** Les mainteneurs de paquets doivent impérativement activer l'authentification multifacteur (MFA) si disponible et surveiller étroitement l'activité de leurs comptes.
*   **Vérification des sources :** Pour les utilisateurs, privilégier les dépôts officiels et inspecter systématiquement les fichiers `PKGBUILD` avant toute compilation ou installation, particulièrement pour les paquets peu maintenus.
*   **Gestion des dépôts :** Les administrateurs de l'AUR doivent renforcer les procédures de vetting pour les nouveaux mainteneurs prenant en charge des paquets orphelins.

---
[Source](https://www.schneier.com/blog/archives/2026/06/friday-squid-blogging-squid-inspired-fluid-pump.html){:target="_blank"}
