---
title: 'D-Link warns of max severity zero-day bug in DIR-822A routers'
date: 2026-09-22
permalink: /posts/2026/09/22/d-link-warns-of-max-severity-zero-day-bug-in-dir-822a-routers/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités critiques sur les routeurs D-Link DIR-822A

D-Link a émis une alerte concernant deux vulnérabilités majeures affectant les routeurs Wi-Fi legacy DIR-822A. Des preuves de concept (PoC) sont déjà publiques pour les deux failles, augmentant considérablement le risque d'exploitation active.

**Points clés :**
*   Les deux failles permettent une corruption de la mémoire pouvant mener à l'exécution de code à distance ou au plantage des appareils.
*   Aucun correctif n'est disponible pour le moment ; D-Link mène actuellement des investigations.
*   Ces vulnérabilités ciblent des composants réseau spécifiques (serveur DHCP et parser L2TP).

**Vulnérabilités identifiées :**
*   **CVE-2026-86296 :** Dépassement de tampon basé sur la pile (stack-based buffer overflow) dans le serveur DHCP. Exploitable à distance sans authentification par l'envoi de paquets DHCP spécialement conçus.
*   **CVE-2026-86510 :** Écriture hors limites (out-of-bounds write) dans le parser de messages de contrôle L2TP. Nécessite des privilèges de base pour manipuler les données d'entrée.

**Recommandations de sécurité :**
*   **Isoler le matériel :** S'assurer que les routeurs ne sont pas exposés directement sur Internet.
*   **Restreindre l'accès :** Désactiver l'administration à distance et limiter l'accès à l'interface d'administration aux seuls utilisateurs et systèmes de confiance via un pare-feu ou des contrôles d'accès réseau.
*   **Surveillance :** Être vigilant face à d'éventuelles tentatives d'intrusion, ces modèles étant fréquemment ciblés pour l'intégration dans des botnets DDoS.

---
[Source](https://www.bleepingcomputer.com/news/security/d-link-warns-of-max-severity-zero-day-bug-in-dir-822a-routers/){:target="_blank"}
