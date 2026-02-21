---
title: 'AI-Assisted Threat Actor Compromises 600+ FortiGate Devices in 55 Countries'
date: 2026-02-21
permalink: /posts/2026/02/21/ai-assisted-threat-actor-compromises-600-fortigate-devices-in-55-countries/
tags:
- veille-cyber
- hackernews
---
## L'IA au service de cybercriminels : une menace amplifiée pour les équipements FortiGate

Un groupe de cyberattaquants russophones, motivé par des gains financiers, a exploité des services d'intelligence artificielle générative (IA) pour compromettre plus de 600 appareils FortiGate dans 55 pays. Cette campagne, observée entre janvier et février 2026, ne repose pas sur l'exploitation de vulnérabilités logicielles spécifiques, mais plutôt sur des failles fondamentales : des ports de gestion exposés sur Internet et l'utilisation de mots de passe faibles avec authentification à facteur unique.

L'IA a permis à cet acteur, aux capacités techniques limitées, d'automatiser et d'amplifier diverses phases de ses attaques, allant du développement d'outils à la génération de commandes. L'utilisation de plusieurs outils d'IA, y compris une solution de secours pour la reconnaissance dans les réseaux compromis, témoigne d'une approche structurée inspirée d'une "chaîne de montage de cybercriminalité assistée par IA".

Les conséquences de ces compromissions incluent l'accès aux environnements Active Directory, l'extraction de bases de données d'identifiants, et des tentatives de ciblage des infrastructures de sauvegarde, suggérant une préparation en vue de déploiements de ransomwares. L'acteur cible les victimes les plus accessibles, profitant de son manque d'expertise pour identifier des "proies faciles".

Les méthodes d'attaque impliquaient le scan systématique des interfaces de gestion FortiGate exposées sur Internet, suivi de tentatives d'authentification avec des identifiants couramment réutilisés. L'exploitation des données volées permettait ensuite des activités post-exploitation comme la reconnaissance, la compromission d'Active Directory, et l'accès aux systèmes de sauvegarde, notamment en exploitant des vulnérabilités connues sur des solutions comme Veeam Backup & Replication.

### Points Clés :

*   **Outil IA utilisé :** Des services commerciaux d'IA générative pour le développement d'outils, la planification d'attaques et la génération de commandes.
*   **Faiblesse exploitée :** Ports de gestion FortiGate exposés sur Internet et mots de passe faibles avec authentification unique.
*   **Objectif :** Gains financiers, avec des indices d'une préparation à des attaques par ransomware.
*   **Portée :** Plus de 600 appareils FortiGate dans 55 pays.
*   **Méthode :** Scan automatisé d'interfaces de gestion exposées, authentification par identifiants faibles, puis activités post-exploitation avancées.

### Vulnérabilités exploitées :

*   Pas de vulnérabilités logicielles spécifiques à FortiGate mentionnées dans l'article. L'attaque repose sur des failles de configuration et de sécurité fondamentales.
*   **Veeam Backup & Replication :**
    *   CVE-2023-27532 (mentionnée comme potentiellement exploitée)
    *   CVE-2024-40711 (mentionnée comme potentiellement exploitée)

### Recommandations :

*   **Sécurité des appliances FortiGate :**
    *   Ne pas exposer les interfaces d'administration sur Internet.
    *   Changer les identifiants par défaut et couramment utilisés.
    *   Implémenter l'authentification multifacteur (MFA) pour l'accès administratif et VPN.
    *   Auditer les comptes administratifs et les connexions pour détecter toute activité non autorisée.
    *   Rotation des identifiants des utilisateurs VPN SSL.
*   **Sécurité générale du réseau :**
    *   Isoler les serveurs de sauvegarde de l'accès réseau général.
    *   Maintenir tous les logiciels à jour.
    *   Surveiller l'exposition réseau non intentionnelle.
    *   Gérer les correctifs pour les appareils périmétriques.
    *   Appliquer une bonne hygiène des identifiants.
    *   Mettre en œuvre la segmentation réseau.
    *   Disposer de détections robustes pour les indicateurs de post-exploitation.

---
[Source](https://thehackernews.com/2026/02/ai-assisted-threat-actor-compromises.html){:target="_blank"}
