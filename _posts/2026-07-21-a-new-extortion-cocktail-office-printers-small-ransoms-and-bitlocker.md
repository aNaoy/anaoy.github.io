---
title: 'A new extortion cocktail: office printers, small ransoms, and BitLocker'
date: 2026-07-21
permalink: /posts/2026/07/21/a-new-extortion-cocktail-office-printers-small-ransoms-and-bitlocker/
tags:
- veille-cyber
- securelist
---
### L'extorsion par BitLocker : détournement d'outils légitimes et impression de rançons

Des campagnes d'extorsion récentes exploitent des outils système natifs comme **BitLocker** pour chiffrer les données des entreprises, tout en utilisant les imprimantes réseau pour diffuser les demandes de rançon. Les attaquants, tels que le groupe "XEntry Team", privilégient cette méthode plutôt que le recours à des rançongiciels classiques (ransomware-as-a-service).

**Points clés :**
*   **Mode opératoire :** Après intrusion, les attaquants utilisent des outils de gestion à distance (RMM) ou des GPO pour activer BitLocker à grande échelle.
*   **Détournement d'outils :** Le chiffrement repose exclusivement sur des fonctionnalités légitimes de Windows, rendant la détection par les antivirus traditionnels plus complexe si les alertes sont ignorées.
*   **Signe distinctif :** L'usage des imprimantes de l'entreprise pour imprimer physiquement les messages de rançon.
*   **Persistance :** Installation d'outils de gestion à distance (Mesh Agent, Tactical RMM) pour maintenir l'accès.

**Vulnérabilités exploitées :**
*   **Exposition RDP :** Services Bureau à distance accessibles directement sur Internet sans contrôle strict.
*   **Configuration MSSQL :** Utilisation de la procédure stockée `xp_cmdshell` pour l'exécution de commandes système.
*   **Gestion des accès :** Identifiants de connexion exposés publiquement (ex: GitHub).
*   **Absence de surveillance :** Non-traitement des alertes de sécurité EPP et désactivation de protections pour raisons de compatibilité.

**Recommandations :**
*   **Sécuriser les accès :** Interdire l'exposition directe du protocole RDP sur Internet et limiter l'accès via VPN ou passerelles sécurisées.
*   **Durcir les serveurs :** Désactiver les fonctionnalités inutiles (ex: `xp_cmdshell` sur SQL Server) et appliquer le principe du moindre privilège.
*   **Renforcer la surveillance :** Centraliser les journaux d'événements et traiter systématiquement les alertes remontées par les solutions EPP/EDR.
*   **Contrôle des applications :** Restreindre l'installation et l'exécution d'outils RMM non autorisés.
*   **Plan de réponse aux incidents :** Éviter une restauration précipitée des systèmes afin de préserver les preuves numériques nécessaires à l'analyse médico-légale et à la compréhension de l'intrusion.

---
[Source](https://securelist.com/new-extortion-scheme-printers-bitlocker/120718/){:target="_blank"}
