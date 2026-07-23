---
title: 'New RefluXFS Linux flaw lets attackers gain root privileges'
date: 2026-07-23
permalink: /posts/2026/07/23/new-refluxfs-linux-flaw-lets-attackers-gain-root-privileges/
tags:
- veille-cyber
- bleepingcomp
---
### RefluXFS : Vulnérabilité critique d'escalade de privilèges sous Linux

Une faille de type « race condition » (condition de compétition) vieille de neuf ans, baptisée **RefluXFS**, affecte le système de fichiers XFS des noyaux Linux (v4.11 et ultérieures). Identifiée par l'unité de recherche de Qualys avec l'assistance de l'IA Claude Mythos, cette vulnérabilité permet à un utilisateur local non privilégié d'écraser des fichiers protégés (fichiers de configuration root ou binaires SUID-root) pour obtenir les privilèges super-utilisateur.

**Points clés :**
*   **Vulnérabilité :** CVE-2026-64600.
*   **Mécanisme :** Exploitation d'une fenêtre de vulnérabilité lors du processus « copy-on-write » dans le système de fichiers XFS avec *reflink* activé.
*   **Persistance :** Les modifications sont écrites directement sur le disque, persistent après un redémarrage et ne génèrent aucun journal système.
*   **Contournement des défenses :** La faille opérant au niveau de la couche d'allocation du système de fichiers, elle neutralise les protections habituelles comme SELinux, KASLR, SMEP, SMAP ou l'isolation des conteneurs.
*   **Impact :** Concerne les principales distributions d'entreprise (RHEL, Oracle Linux, Amazon Linux, Fedora, Rocky Linux, AlmaLinux, etc.), soit potentiellement plus de 16,4 millions de systèmes.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs du noyau fournis par les éditeurs de distribution (le correctif officiel a été intégré le 16 juillet).
*   **Redémarrage :** Un redémarrage du système est indispensable pour que la mise à jour soit effective.
*   **Priorisation :** Les systèmes multi-utilisateurs et les serveurs exposés doivent être traités en priorité, aucune mitigation alternative n'étant actuellement viable.

---
[Source](https://www.bleepingcomputer.com/news/linux/new-refluxfs-linux-flaw-lets-attackers-gain-root-privileges/){:target="_blank"}
