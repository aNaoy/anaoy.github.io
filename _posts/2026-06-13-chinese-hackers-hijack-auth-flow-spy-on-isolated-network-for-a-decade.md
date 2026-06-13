---
title: 'Chinese hackers hijack auth flow, spy on isolated network for a decade'
date: 2026-06-13
permalink: /posts/2026/06/13/chinese-hackers-hijack-auth-flow-spy-on-isolated-network-for-a-decade/
tags:
- veille-cyber
- bleepingcomp
---
### Opération Highland : Une décennie d'espionnage par Velvet Ant

Le groupe de cyberespionnage chinois « Velvet Ant » a maintenu un accès persistant pendant dix ans au sein d'une infrastructure critique, en compromettant des systèmes exposés sur Internet pour s'infiltrer dans un réseau isolé (air-gapped).

**Points clés :**
*   **Stratégie de pivot :** Après avoir pris pied sur des serveurs internet, les attaquants ont utilisé des proxies SOCKS5 personnalisés pour naviguer latéralement.
*   **Accès au réseau isolé :** L'accès a été rendu possible via le chaînage de requêtes HTTP transmises par des serveurs Nginx compromis, redirigeant les commandes vers des processus internes (FastCGI/fcgiwrap).
*   **Détournement de l'authentification :** Le groupe a remplacé les modules PAM (*Pluggable Authentication Modules*) et les composants OpenSSH par des versions malveillantes. Cela leur a permis de récolter des identifiants en temps réel et de contourner les mesures de sécurité classiques, rendant leur présence invisible aux administrateurs.
*   **Difficulté de remédiation :** L'imbrication des composants malveillants dans le cœur du système a nécessité une planification rigoureuse pour éviter de bloquer l'accès légitime lors du nettoyage.

**Vulnérabilités :**
Bien que l'article mentionne des exploitations passées, il cite spécifiquement :
*   **Cisco NX-OS :** Utilisation d'une vulnérabilité zero-day (non spécifiée par CVE dans le texte) sur des switchs Nexus.
*   **F5 BIG-IP :** Campagnes antérieures utilisant des failles non détaillées sur ces équipements.

**Recommandations :**
*   **Sécurisation des composants critiques :** Traiter PAM, OpenSSH et LSASS comme des actifs de haute sécurité, sous surveillance étroite (EDR, intégrité des fichiers).
*   **Gestion des accès :** Implémenter une authentification multifacteur (MFA) robuste et durcir les accès à privilèges.
*   **Stratégie de récupération :** Mettre en place des sauvegardes immuables et planifier des procédures de restauration hors ligne testées régulièrement.
*   **Monitoring :** Détecter toute modification non autorisée des bibliothèques système et des configurations de services web utilisés pour le routage interne.

---
[Source](https://www.bleepingcomputer.com/news/security/chinese-hackers-hijack-auth-flow-spy-on-isolated-network-for-a-decade/){:target="_blank"}
