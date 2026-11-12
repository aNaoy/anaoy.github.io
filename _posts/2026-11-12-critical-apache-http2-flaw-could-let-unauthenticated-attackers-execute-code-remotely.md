---
title: 'Critical Apache HTTP/2 Flaw Could Let Unauthenticated Attackers Execute Code Remotely'
date: 2026-11-12
permalink: /posts/2026/11/12/critical-apache-http2-flaw-could-let-unauthenticated-attackers-execute-code-remotely/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique d'exécution de code dans Apache HTTP/2

Une faille critique a été identifiée dans le module `mod_http2` du serveur Apache HTTP, permettant à un attaquant non authentifié d'exécuter du code à distance et de prendre potentiellement le contrôle complet du processus serveur.

**Points clés :**
*   **Vulnérabilité :** CVE-2026-119618 (Score CVSS : 9.8).
*   **Impact :** Exécution de code à distance (RCE) sans authentification.
*   **Versions affectées :** 
    *   Apache HTTP Server : 2.4.55 à 2.4.70.
    *   `mod_h2` (standalone) : 2.0.8 à 2.0.42.
*   **Conditions :** La faille ne concerne que les serveurs ayant le protocole HTTP/2 activé via la directive `Protocols` (h2 ou h2c).
*   **Origine :** Découverte initialement par le scanner OSS d'Anthropic, puis signalée par Google Cloud Vulnerability Research.

**Recommandations :**
*   **Mise à jour :** Appliquer immédiatement la version **2.4.71** du serveur Apache HTTP ou mettre à jour les paquets fournis par les distributions Linux (ex: RHEL 9 et 10 disposent déjà de correctifs).
*   **Atténuation temporaire :** Pour les systèmes ne pouvant être mis à jour, désactiver le support HTTP/2 en modifiant la directive `Protocols` dans la configuration du serveur (ou des hôtes virtuels) pour ne conserver que `http/1.1`.
*   **Vérification :** Inspecter l'ensemble des configurations de serveurs et d'hôtes virtuels, car le protocole peut être activé à différents niveaux.

---
[Source](https://thehackernews.com/2026/11/critical-apache-http2-flaw-could-let.html){:target="_blank"}
