---
title: 'Chinese hackers breach REDCap servers, steal medical research'
date: 2026-06-15
permalink: /posts/2026/06/15/chinese-hackers-breach-redcap-servers-steal-medical-research/
tags:
- veille-cyber
- bleepingcomp
---
### Espionnage informatique : Le malware InfiniteRed cible les serveurs REDCap

Le groupe de cyberespionnage chinois UNC6508 a infiltré des institutions de recherche médicale nord-américaines via les serveurs REDCap, compromettant des données sensibles pendant plus d'un an (septembre 2023 - novembre 2025).

**Points clés :**
*   **Malware InfiniteRed :** Un logiciel malveillant furtif conçu pour REDCap, composé d'un module de persistance, d'un collecteur d'identifiants et d'une porte dérobée (backdoor).
*   **Technique d'exfiltration innovante :** Les attaquants ont détourné les règles de « conformité de contenu » des outils de productivité cloud pour scanner et envoyer automatiquement les données sensibles par e-mail vers des comptes externes.
*   **Cibles :** Recherche médicale, essais cliniques, santé publique et sujets stratégiques/militaires.
*   **Opérations discrètes :** Utilisation de proxys résidentiels aux États-Unis, de routeurs compromis et de serveurs VPS pour masquer leur origine.

**Vulnérabilités :**
*   Le vecteur initial repose sur l'exploitation d'anciennes versions vulnérables de la plateforme REDCap. Bien qu'aucune CVE spécifique ne soit citée, le rapport souligne une exploitation proactive des instances obsolètes.

**Recommandations :**
*   **Mise à jour immédiate :** Passer aux versions les plus récentes de REDCap et supprimer les déploiements hérités (legacy).
*   **Sécurisation des accès :** Implémenter l'authentification multifacteur (MFA/2SV) sur tous les comptes à privilèges.
*   **Protection des sessions :** Utiliser les « Device Bound Session Credentials » (DBSC) pour contrer le vol de sessions.
*   **Détection :** Utiliser les règles YARA et les indicateurs de compromission (IoCs) fournis par Google Threat Intelligence pour auditer les environnements.

---
[Source](https://www.bleepingcomputer.com/news/security/chinese-hackers-breach-redcap-servers-steal-medical-research/){:target="_blank"}
