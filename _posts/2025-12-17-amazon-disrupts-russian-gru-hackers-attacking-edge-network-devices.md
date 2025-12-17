---
title: 'Amazon disrupts Russian GRU hackers attacking edge network devices'
date: 2025-12-17
permalink: /posts/2025/12/17/amazon-disrupts-russian-gru-hackers-attacking-edge-network-devices/
tags:
- veille-cyber
- bleepingcomp
---
**Cyberattaques ciblées contre les infrastructures critiques occidentales**

Une campagne de cybersécurité active, attribuée à des pirates informatiques liés au renseignement militaire russe (GRU), a été déjouée par Amazon. Ces attaques, qui ont débuté en 2021, visaient principalement les infrastructures critiques occidentales, notamment le secteur de l'énergie, en s'appuyant sur des dispositifs réseau mal configurés.

**Points clés :**

*   **Évolution des tactiques :** Initialement, les attaquants exploitaient des vulnérabilités connues et inconnues (zero-day). Plus récemment, leur stratégie a évolué vers l'exploitation de dispositifs réseau périphériques mal configurés, tels que les routeurs d'entreprise, les passerelles VPN et les appliances de gestion réseau. Cette approche, considérée comme plus simple ("low-hanging fruit"), permet d'atteindre les mêmes objectifs : accès persistant aux réseaux, vol d'identifiants et reconnaissance sur les services en ligne des organisations ciblées.
*   **Attribution :** Amazon attribue ces attaques avec une grande confiance au GRU russe, en se basant sur les modèles de ciblage et les chevauchements d'infrastructure observés avec des groupes tels que Sandworm (APT44, Seashell Blizzard) et Curly COMrades.
*   **Mécanismes d'action :** Bien que le mécanisme d'extraction des données ne soit pas directement observé, les indices suggèrent l'utilisation de la capture passive de paquets et de l'interception de trafic pour voler des identifiants.
*   **Impact limité sur AWS :** Les attaques exploitaient des dispositifs réseau gérés par les clients et hébergés sur des instances AWS EC2, sans exploiter de failles dans les services AWS eux-mêmes.
*   **Actions d'Amazon :** Amazon a pris des mesures immédiates pour protéger les instances compromises, a informé les clients concernés et a partagé des informations avec les fournisseurs et partenaires de l'industrie. Ces actions ont permis de perturber les opérations des attaquants et de réduire leur surface d'attaque.

**Vulnérabilités exploitées :**

L'article mentionne que par le passé, les attaquants exploitaient des vulnérabilités dans les produits suivants :
*   WatchGuard
*   Confluence
*   Veeam

Aucune CVE spécifique n'est mentionnée dans l'article pour ces vulnérabilités.

**Recommandations :**

*   **Actions prioritaires immédiates :**
    *   Auditer les dispositifs réseau.
    *   Surveiller les activités de rejeu d'identifiants.
    *   Surveiller les accès aux portails administratifs.

*   **Recommandations spécifiques aux environnements AWS :**
    *   Isoler les interfaces de gestion.
    *   Restreindre les groupes de sécurité.
    *   Activer CloudTrail, GuardDuty et VPC Flow Logs.

---
[Source](https://www.bleepingcomputer.com/news/security/amazon-disrupts-russian-gru-hackers-attacking-edge-network-devices/){:target="_blank"}
