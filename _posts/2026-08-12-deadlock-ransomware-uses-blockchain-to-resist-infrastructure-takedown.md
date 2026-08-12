---
title: 'DeadLock ransomware uses blockchain to resist infrastructure takedown'
date: 2026-08-12
permalink: /posts/2026/08/12/deadlock-ransomware-uses-blockchain-to-resist-infrastructure-takedown/
tags:
- veille-cyber
- bleepingcomp
---
### DeadLock : Le rançongiciel résilient basé sur la blockchain

Le groupe DeadLock, actif depuis mi-2025, déploie un rançongiciel utilisant une infrastructure décentralisée pour échapper aux interventions des autorités. Ce malware, utilisé par divers affiliés (notamment d'anciens membres des écosystèmes Lynx et INC), privilégie les tactiques de double extorsion.

**Points clés :**
*   **Infrastructure décentralisée :** Le groupe utilise la blockchain Polygon pour stocker ses configurations et ses serveurs C2 (commande et contrôle). Les victimes communiquent via le réseau sécurisé *Session*, tandis que les données volées sont hébergées sur *Wasabi*.
*   **Chiffrement performant :** Le logiciel malveillant (écrit en Rust) utilise l'algorithme XChaCha20 avec des clés Curve25519. Il est conçu pour optimiser ses ressources (29% de la RAM et 70% du CPU) afin de ne pas ralentir le système cible pendant le chiffrement.
*   **Ciblage :** Le logiciel évite les pays de l'ex-URSS, la CEI, ainsi que l'Iran, la Syrie, Oman et le Yémen.
*   **Objectifs :** Plus de 80 entreprises européennes touchées dans les secteurs de l'IT, de l'industrie, du transport et du commerce.

**Vulnérabilités :**
Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur l'exploitation des vecteurs d'accès initiaux (compromission d'identifiants, mouvements latéraux via WMI/PsExec) et non sur une faille logicielle unique. La résilience de l'infrastructure est toutefois limitée par la dépendance aux nœuds RPC publics de Polygon et aux hébergeurs de fichiers (Wasabi).

**Recommandations :**
*   **Protection des points de terminaison :** Activer les solutions antivirus basées sur le cloud, le mode blocage EDR et la protection anti-altération.
*   **Réduction de la surface d'attaque :** Appliquer des règles pour bloquer les exécutables non approuvés et limiter les mouvements latéraux (WMI, PsExec).
*   **Contrôle des fichiers :** Utiliser la fonctionnalité "Accès contrôlé aux dossiers" (Controlled Folder Access) pour empêcher les modifications non autorisées par des processus suspects.
*   **Réponse aux incidents :** Automatiser les processus d'investigation et de remédiation pour stopper les attaques dès les premiers signes de compromission.

---
[Source](https://www.bleepingcomputer.com/news/security/deadlock-ransomware-uses-blockchain-to-resist-infrastructure-takedown/){:target="_blank"}
