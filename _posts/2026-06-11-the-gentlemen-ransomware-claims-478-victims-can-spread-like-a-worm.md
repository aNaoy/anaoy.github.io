---
title: 'The Gentlemen Ransomware Claims 478 Victims, Can Spread Like a Worm'
date: 2026-06-11
permalink: /posts/2026/06/11/the-gentlemen-ransomware-claims-478-victims-can-spread-like-a-worm/
tags:
- veille-cyber
- hackernews
---
### Analyse du groupe de ransomware "The Gentlemen" (Phantom Mantis)

Le groupe **The Gentlemen** (suivi sous le nom de Phantom Mantis ou Storm-2697) est une opération de ransomware indépendante et hautement organisée, dirigée par le cybercriminel russe Alexander Andreevich Yapaev (alias LARVA-368). Actif depuis mars 2025, le groupe a déjà revendiqué 478 victimes en utilisant un modèle de RaaS (Ransomware-as-a-Service) agressif avec un partage de revenus de 90 % pour ses affiliés.

#### Points clés
*   **Évolution :** Issu d'anciennes affiliations (LockBit, Qilin, Medusa), le groupe a pris son indépendance en juillet 2025 à la suite de différends financiers.
*   **Techniques d'attaque :** Utilisation intensive de l'IA pour le développement, adoption de la technique **BYOVD** (Bring Your Own Vulnerable Driver) pour désactiver les EDR, et recours à des outils de "Red Teaming" (NetExec, Velociraptor).
*   **Capacités de propagation :** Le malware, écrit en Go et obfusqué avec Garble, peut fonctionner comme un ver informatique auto-propageable au sein des réseaux compromis.
*   **Vecteurs d'accès :** Exploitation prioritaire d'équipements périphériques exposés (VPN, pare-feux Cisco et Fortinet) et abus de comptes privilégiés.
*   **Modèle d'extorsion :** Double extorsion combinant chiffrement, exfiltration de données, harcèlement par email et appels téléphoniques.

#### Vulnérabilités exploitées
Le groupe intègre activement des failles récentes dans ses pipelines d'exploitation pour maintenir sa flexibilité :
*   **CVE-2024-55591**
*   **CVE-2025-32433**
*   **CVE-2025-33073**
*   Exploitation régulière de vulnérabilités connues dans les produits VMware Aria, Fortinet, Cisco et Microsoft.

#### Recommandations de sécurité
*   **Renforcement du périmètre :** Appliquer immédiatement les correctifs sur les équipements de périphérie (VPN, firewalls) et limiter strictement leur exposition sur Internet.
*   **Gestion des accès :** Implémenter le principe du moindre privilège, surveiller les abus de comptes administrateurs et sécuriser l'Active Directory.
*   **Protection des endpoints :** Déployer des solutions EDR capables de détecter les techniques de contournement comme le BYOVD et surveiller les comportements anormaux liés aux outils de type "Red Team".
*   **Stratégie de sauvegarde :** Maintenir des sauvegardes immuables et déconnectées du réseau, en gardant à l'esprit que le groupe cible spécifiquement les infrastructures VMware.
*   **Veille et monitoring :** Surveiller les journaux d'événements Windows (System, Application, Security) pour détecter toute tentative de nettoyage ou de désactivation de Microsoft Defender par les attaquants.

---
[Source](https://thehackernews.com/2026/06/the-gentlemen-ransomware-claims-478.html){:target="_blank"}
