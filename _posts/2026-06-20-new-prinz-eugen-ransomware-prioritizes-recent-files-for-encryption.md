---
title: 'New Prinz Eugen ransomware prioritizes recent files for encryption'
date: 2026-06-20
permalink: /posts/2026/06/20/new-prinz-eugen-ransomware-prioritizes-recent-files-for-encryption/
tags:
- veille-cyber
- bleepingcomp
---
### Prinz Eugen : Un ransomware tactique axé sur les fichiers récents

Le groupe de ransomware « Prinz Eugen » se distingue par une approche manuelle ("hands-on-keyboard") et l'absence de modèle RaaS (Ransomware-as-a-Service). Contrairement aux opérations classiques, ce groupe ne dépose aucune note de rançon sur les systèmes infectés afin de minimiser son empreinte numérique et de compliquer la détection automatique.

**Points clés :**
*   **Stratégie de chiffrement :** Le malware, écrit en Go, priorise les fichiers modifiés récemment pour maximiser l'impact opérationnel sur l'activité des victimes.
*   **Techniques d'intrusion :** Utilisation probable d'identifiants RDP compromis, couplée à l'usage d'outils d'administration à distance (RMM) légitimes comme RemotePC.
*   **Persistance :** Création de comptes administrateurs dérobés (backdoors) pour maintenir l'accès au réseau.
*   **Méthodologie d'extorsion :** Communication hors-bande (e-mail, portail web ou téléphone) pour éviter de laisser des preuves forensiques sur la machine.
*   **Chiffrement technique :** Utilisation de l'algorithme ChaCha20-Poly1305 avec une vérification d'intégrité SHA-256. Le malware supprime toute trace de la clé de chiffrement en mémoire avant de s'auto-effacer.

**Vulnérabilités exploitées :**
*   Aucune CVE spécifique n'est mentionnée ; l'attaque repose principalement sur l'exploitation d'identifiants RDP faibles ou volés et l'abus d'outils d'administration légitimes (Living-off-the-land).

**Recommandations :**
*   **Sécurisation des accès :** Imposer l'authentification multifacteur (MFA) pour tous les accès distants, en particulier le RDP.
*   **Surveillance RMM :** Auditer strictement l'utilisation des logiciels de contrôle à distance et restreindre leur déploiement aux administrateurs autorisés.
*   **Gestion des identités :** Chasser les comptes administrateurs non autorisés ou créés récemment dans l'Active Directory.
*   **Détection :** S'appuyer sur les Indicateurs de Compromission (IoC) fournis dans le rapport technique de Threatdown pour renforcer les règles EDR et SIEM.
*   **Sauvegardes :** Maintenir des sauvegardes immuables et isolées du réseau pour garantir une restauration rapide sans avoir à négocier avec les attaquants.

---
[Source](https://www.bleepingcomputer.com/news/security/new-prinz-eugen-ransomware-prioritizes-recent-files-for-encryption/){:target="_blank"}
