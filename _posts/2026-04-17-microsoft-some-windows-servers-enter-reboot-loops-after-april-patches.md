---
title: 'Microsoft: Some Windows servers enter reboot loops after April patches'
date: 2026-04-17
permalink: /posts/2026/04/17/microsoft-some-windows-servers-enter-reboot-loops-after-april-patches/
tags:
- veille-cyber
- bleepingcomp
---
### Instabilité des serveurs Windows après la mise à jour d'avril 2026

Suite au déploiement de la mise à jour de sécurité KB5082063, certains contrôleurs de domaine Windows subissent des boucles de redémarrage critiques. Le problème provient d'une défaillance du service LSASS (*Local Security Authority Subsystem Service*) au démarrage, bloquant les services d'authentification et l'accès au domaine.

**Points clés :**
* **Cause :** Conflit lors du traitement des requêtes d'authentification en phase de démarrage.
* **Environnements impactés :** Systèmes utilisant la gestion des accès privilégiés (PAM) et serveurs non-Global Catalog (non-GC).
* **Versions touchées :** Windows Server 2025, 2022, 23H2, 2019 et 2016.
* **Problèmes connexes :** Microsoft enquête également sur des échecs d'installation de la mise à jour KB5082063 sur Windows Server 2025 et sur des demandes imprévues de clés BitLocker.

**Vulnérabilités :**
* Aucun CVE n'est associé à cet incident ; il s'agit d'une instabilité logicielle induite par une mise à jour système.

**Recommandations :**
* Si le déploiement a causé des instabilités, il est conseillé de ne pas tenter de résolutions manuelles complexes.
* Contacter le **Support Microsoft for Business** afin d'obtenir les mesures d'atténuation spécifiques pour votre configuration, en attendant la publication d'un correctif officiel.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-warns-of-reboot-loops-affecting-some-domain-controllers/){:target="_blank"}
