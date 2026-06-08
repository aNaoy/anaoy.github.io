---
title: 'Check Point links VPN zero-day attacks to Qilin ransomware gang'
date: 2026-06-08
permalink: /posts/2026/06/08/check-point-links-vpn-zero-day-attacks-to-qilin-ransomware-gang/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités critiques dans les solutions VPN de Check Point exploitées par le groupe Qilin

Check Point a publié des correctifs pour deux vulnérabilités critiques affectant ses solutions VPN. Ces failles concernent spécifiquement les déploiements utilisant le protocole obsolète IKEv1. Des attaques « zero-day » ont été observées, avec une implication confirmée du groupe de ransomware Qilin.

**Points clés :**
*   **Cible :** Les passerelles utilisant le protocole IKEv1 sans exigence de certificat machine.
*   **Activité malveillante :** Des attaques actives ont débuté le 7 mai, touchant quelques dizaines d'organisations mondiales.
*   **Menace associée :** Le groupe de ransomware Qilin, connu pour ses attaques contre de grandes entreprises et institutions, a été lié à l'exploitation de ces vulnérabilités.

**Vulnérabilités :**
*   **CVE-2026-50751 :** Vulnérabilité de contournement d'authentification critique permettant à des attaquants distants non authentifiés d'établir une connexion VPN.
*   **CVE-2026-50752 :** Problème de validation de certificat dans le protocole IKEv1, susceptible d'être exploité lors d'attaques de type « homme du milieu » (Man-in-the-Middle) sur des connexions VPN site-à-site.

**Recommandations :**
*   **Appliquer les correctifs :** Installer immédiatement les mises à jour de sécurité fournies par Check Point.
*   **Sécuriser la configuration :**
    *   Migrer exclusivement vers le protocole **IKEv2**.
    *   Rendre l'authentification par **certificat machine obligatoire**.
    *   Supprimer la prise en charge des clients d'accès à distance obsolètes.
*   **Protection supplémentaire :** Activer le système de prévention d'intrusion (IPS) et mettre à jour ses signatures.

---
[Source](https://www.bleepingcomputer.com/news/security/check-point-links-vpn-zero-day-attacks-to-qilin-ransomware-gang/){:target="_blank"}
