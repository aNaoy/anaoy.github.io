---
title: 'Windows LegacyHive zero-day flaw gets free, unofficial patches'
date: 2026-07-21
permalink: /posts/2026/07/21/windows-legacyhive-zero-day-flaw-gets-free-unofficial-patches/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité LegacyHive : Correctifs non officiels disponibles

Une nouvelle faille « zero-day » affectant le service de profil utilisateur de Windows, baptisée **LegacyHive**, a été découverte par le chercheur en sécurité « Nightmare Eclipse ». Elle permet à un utilisateur non privilégié d'élever ses privilèges et d'exécuter du code arbitraire en manipulant la base de registre.

**Points clés :**
*   **Mécanisme :** La vulnérabilité permet de monter la ruche de registre d'un autre utilisateur en mode accès complet, facilitant le vol de secrets ou l'injection de commandes qui s'exécuteront lors de la prochaine connexion d'un administrateur.
*   **Statut :** Microsoft est informé mais n'a pas encore publié de correctif officiel ni attribué d'identifiant CVE.
*   **Détection :** Des requêtes de chasse aux menaces pour Microsoft Defender for Endpoint ont été publiées par l'expert Kevin Beaumont pour identifier les tentatives d'exploitation.

**Vulnérabilités :**
*   **Nom :** LegacyHive
*   **CVE :** Non attribué (à ce jour).
*   **Systèmes impactés :** Windows 10 (version 2004 et ultérieures) et Windows Server 2019/2022 et ultérieurs.

**Recommandations :**
*   **Appliquer un micro-correctif :** En l'absence de mise à jour officielle, la société ACROS Security propose via sa plateforme **0Patch** des micro-correctifs gratuits qui neutralisent l'exploitation en empêchant le chargement de la ruche utilisateur ciblée.
*   **Surveillance :** Utiliser les requêtes KQL (disponibles sur GitHub) au sein de Microsoft Defender pour détecter toute activité suspecte liée à cette faille sur le parc informatique.

---
[Source](https://www.bleepingcomputer.com/news/security/windows-legacyhive-zero-day-flaw-gets-free-unofficial-patches/){:target="_blank"}
