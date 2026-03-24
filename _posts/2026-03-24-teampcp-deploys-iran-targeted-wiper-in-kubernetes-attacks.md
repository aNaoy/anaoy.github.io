---
title: 'TeamPCP deploys Iran-targeted wiper in Kubernetes attacks'
date: 2026-03-24
permalink: /posts/2026/03/24/teampcp-deploys-iran-targeted-wiper-in-kubernetes-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Offensive cybernétique de TeamPCP : Sabotage sélectif et persistance dans Kubernetes

Le groupe de hackers TeamPCP déploie une campagne malveillante sophistiquée visant les clusters Kubernetes, utilisant une infrastructure partagée avec la campagne « CanisterWorm ». La menace se distingue par un comportement destructeur sélectif basé sur la géolocalisation.

**Points clés :**
*   **Sabotage ciblé :** Les systèmes identifiés comme iraniens (fuseau horaire et paramètres régionaux) subissent une destruction totale des données. Si le cluster Kubernetes est présent, un *DaemonSet* privilégié (« Host-provisioner-iran ») efface le système de fichiers hôte avant de forcer un redémarrage. Hors Kubernetes, le script tente une suppression récursive (`rm -rf / --no-preserve-root`) avec élévation de privilèges si nécessaire.
*   **Persistance persistante :** Sur les systèmes non iraniens, le malware déploie un *DaemonSet* (« host-provisioner-std ») qui installe une porte dérobée Python persistante en tant que service *systemd*.
*   **Évolution des tactiques :** TeamPCP a récemment abandonné la propagation latérale via Kubernetes dans certaines variantes pour privilégier la propagation via SSH, en utilisant des clés privées volées et les journaux d'authentification.
*   **Indicateurs d'activité :** Connexions SSH sortantes avec `StrictHostKeyChecking=no`, accès non authentifiés à l'API Docker sur le port 2375, et conteneurs Alpine privilégiés montant le système de fichiers racine de l'hôte.

**Vulnérabilités :**
*   Bien qu'aucune CVE spécifique ne soit mentionnée, l'attaque exploite principalement :
    *   **L'exposition de l'API Docker :** L'absence d'authentification sur le port 2375 permet aux attaquants de déployer des conteneurs privilégiés.
    *   **Mauvaises configurations Kubernetes :** Utilisation excessive de privilèges et montage du système de fichiers hôte (`hostPath`), facilitant l'évasion de conteneur et le sabotage.

**Recommandations :**
*   **Sécuriser l'API Docker :** Désactiver l'accès réseau à l'API Docker ou mettre en place une authentification mutuelle TLS stricte.
*   **Durcir Kubernetes :** Appliquer le principe du moindre privilège, interdire l'utilisation de conteneurs privilégiés via des politiques de sécurité (Pod Security Admission) et limiter strictement les accès en écriture sur le système de fichiers de l'hôte (`hostPath`).
*   **Surveillance réseau :** Surveiller les connexions sortantes suspectes vers le port 2375 et les tentatives de connexions SSH inhabituelles au sein du sous-réseau local.
*   **Gestion des identités :** Auditer régulièrement les clés SSH stockées sur les serveurs et limiter les accès sudo.

---
[Source](https://www.bleepingcomputer.com/news/security/teampcp-deploys-iran-targeted-wiper-in-kubernetes-attacks/){:target="_blank"}
