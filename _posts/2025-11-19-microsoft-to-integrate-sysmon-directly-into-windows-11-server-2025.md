---
title: 'Microsoft to integrate Sysmon directly into Windows 11, Server 2025'
date: 2025-11-19
permalink: /posts/2025/11/19/microsoft-to-integrate-sysmon-directly-into-windows-11-server-2025/
tags:
- veille-cyber
- bleepingcomp
---
**Intégration Native de Sysmon dans Windows pour une Sécurité Renforcée**

Microsoft intégrera prochainement Sysmon nativement dans Windows 11 et Windows Server 2025. Cette évolution permettra de surveiller et d'enregistrer les activités suspectes sur le système, telles que la création et la terminaison de processus, les connexions réseau, les accès aux processus (pour la détection de vol d'identifiants), la création de fichiers exécutables, et les tentatives de manipulation de processus. L'outil, historiquement un utilitaire Sysinternals à installer séparément, deviendra une fonctionnalité intégrée accessible via les "Fonctionnalités optionnelles" de Windows.

**Points Clés :**

*   Sysmon sera intégré nativement dans Windows 11 et Windows Server 2025 l'année prochaine.
*   L'intégration facilitera le déploiement, la gestion et la mise à jour via Windows Update.
*   La fonctionnalité conserve la capacité de Sysmon à utiliser des fichiers de configuration personnalisés pour filtrer les événements.
*   Microsoft publiera une documentation complète et introduira de nouvelles fonctionnalités de gestion d'entreprise et de détection basée sur l'IA.

**Vulnérabilités / Activités Surveillées (Exemples d'Event IDs) :**

*   **Event ID 1 :** Création de processus (utile pour détecter des commandes suspectes).
*   **Event ID 3 :** Connexion réseau (pour la détection d'activités anormales ou de communication C2).
*   **Event ID 8 :** Accès aux processus (peut révéler des tentatives d'accès à LSASS pour du vol d'identifiants).
*   **Event ID 11 :** Création de fichier (pour suivre la génération de scripts utilisés dans le staging de logiciels malveillants).
*   **Event ID 25 :** Manipulation de processus (aide à identifier des techniques d'évasion comme le "process hollowing").
*   **Event IDs 20 & 21 :** Événements WMI (capture d'activités persistantes via les consommateurs et filtres WMI).

**Recommandations :**

*   Configurer Sysmon avec des fichiers de configuration personnalisés pour une surveillance avancée et ciblée.
*   Exploiter les journaux d'événements générés par Sysmon pour la chasse aux menaces et le diagnostic d'incidents.
*   Les administrateurs pourront activer Sysmon via l'invite de commandes (commande `sysmon -i`) et le déployer avec des configurations personnalisées (commande `sysmon -i <nom_du_fichier_config>`).

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-to-integrate-sysmon-directly-into-windows-11-server-2025/){:target="_blank"}
