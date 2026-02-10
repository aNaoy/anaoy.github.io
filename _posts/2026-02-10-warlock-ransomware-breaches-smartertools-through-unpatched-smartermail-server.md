---
title: 'Warlock Ransomware Breaches SmarterTools Through Unpatched SmarterMail Server'
date: 2026-02-10
permalink: /posts/2026/02/10/warlock-ransomware-breaches-smartertools-through-unpatched-smartermail-server/
tags:
- veille-cyber
- hackernews
---
**Ransomware Warlock exploite une faille de SmarterMail pour infiltrer SmarterTools**

Le groupe de ransomware Warlock (aussi connu sous le nom de Storm-2603) a réussi à pénétrer le réseau de SmarterTools en exploitant une instance de SmarterMail qui n'avait pas été mise à jour. L'incident, survenu le 29 janvier 2026, a touché une douzaine de serveurs Windows au sein du réseau de l'entreprise, ainsi qu'un centre de données secondaire. Les clients hébergés utilisant SmarterTrack ont été les plus impactés.

Après avoir obtenu un accès initial, les attaquants ont patienté plusieurs jours avant de prendre le contrôle d'un serveur Active Directory, de créer de nouveaux comptes utilisateurs, puis de déployer des outils comme Velociraptor et un logiciel de chiffrement.

Plusieurs vulnérabilités dans SmarterMail sont identifiées comme ayant pu être exploitées :

*   **CVE-2025-52691** (score CVSS : 10.0)
*   **CVE-2026-23760** : Permet un contournement d'authentification via une requête HTTP spécialement conçue, autorisant la réinitialisation du mot de passe administrateur.
*   **CVE-2026-24423** (score CVSS : 9.3) : Permet une exécution de code à distance sans authentification via une faiblesse dans l'API ConnectToHub.

SmarterTools a corrigé ces vulnérabilités dans la version Build 9511. Les experts ont observé que les attaquants ont privilégié l'exploitation de CVE-2026-23760, combinée à la fonctionnalité de montage de volume, pour obtenir un contrôle total du système et se fondre dans les flux de travail administratifs légitimes.

**Recommandations :**

*   Mettre à jour SmarterMail vers la dernière version disponible (Build 9526) pour une protection optimale.
*   Isoler les serveurs de messagerie pour bloquer les tentatives de mouvement latéral.

---
[Source](https://thehackernews.com/2026/02/warlock-ransomware-breaches.html){:target="_blank"}
