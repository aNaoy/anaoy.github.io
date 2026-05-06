---
title: 'Why ransomware attacks succeed even when backups exist'
date: 2026-05-06
permalink: /posts/2026/05/06/why-ransomware-attacks-succeed-even-when-backups-exist/
tags:
- veille-cyber
- bleepingcomp
---
### La vulnérabilité des sauvegardes face aux ransomwares

Les ransomwares modernes ne se contentent plus de chiffrer les données de production ; ils ciblent délibérément les infrastructures de sauvegarde pour empêcher toute restauration. La plupart des attaques suivent un processus méthodique : vol d'identifiants, découverte du système de sauvegarde, suppression des points de récupération (clichés VSS, snapshots, fichiers), puis déploiement du chiffrement.

**Points clés :**
*   **L'illusion de sécurité :** Les sauvegardes échouent souvent non pas par absence de données, mais parce qu'elles sont exposées, accessibles et non protégées.
*   **Faiblesses structurelles :** Absence d'isolation réseau entre production et sauvegarde, utilisation d'identifiants partagés, et manque de surveillance dédiée aux outils de sauvegarde.
*   **Techniques d'attaque :** Utilisation des outils d'administration légitimes (techniques « living-off-the-land ») pour manipuler les politiques de rétention et supprimer les sauvegardes via API ou accès console.

**Vulnérabilités critiques :**
Bien que l'article ne liste pas de CVE spécifiques, il souligne des vulnérabilités systémiques :
*   **Sur-privilèges des comptes :** L'accès administrateur unique permet de compromettre l'intégralité de la chaîne de sauvegarde.
*   **Absence d'immuabilité :** Les sauvegardes modifiables peuvent être effacées par tout utilisateur disposant de droits suffisants.
*   **Manque de segmentation :** Les systèmes de sauvegarde partagent le même domaine et les mêmes identifiants que le réseau de production.

**Recommandations pour une stratégie résiliente :**
*   **Immuabilité :** Déployer des stockages immuables (WORM - Write Once, Read Many) pour garantir l'intégrité des données même en cas de compromission administrative.
*   **Séparation des identités :** Appliquer strictement le principe du moindre privilège et généraliser l'authentification multifacteur (MFA).
*   **Isolation :** Segmenter les réseaux pour séparer physiquement ou logiquement les environnements de production et de sauvegarde.
*   **Monitoring et automatisation :** Détecter précocement les anomalies d'activité sur les serveurs de sauvegarde et automatiser les tests de restauration pour valider la viabilité des sauvegardes.
*   **Approche unifiée :** Intégrer les outils de cybersécurité (détection/protection) avec les outils de sauvegarde pour éviter les angles morts.

---
[Source](https://www.bleepingcomputer.com/news/security/why-ransomware-attacks-succeed-even-when-backups-exist/){:target="_blank"}
