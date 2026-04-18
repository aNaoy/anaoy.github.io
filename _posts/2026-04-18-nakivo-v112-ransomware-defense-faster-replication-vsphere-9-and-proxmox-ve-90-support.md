---
title: 'NAKIVO v11.2: Ransomware Defense, Faster Replication, vSphere 9, and Proxmox VE 9.0 Support'
date: 2026-04-18
permalink: /posts/2026/04/18/nakivo-v112-ransomware-defense-faster-replication-vsphere-9-and-proxmox-ve-90-support/
tags:
- veille-cyber
- bleepingcomp
---
### Optimisation de la cyber-résilience avec NAKIVO v11.2

La version 11.2 de NAKIVO Backup & Replication introduit des améliorations majeures axées sur la continuité d'activité et le renforcement de la sécurité des infrastructures virtualisées. Cette mise à jour permet une transition fluide vers les environnements de nouvelle génération tout en modernisant les protocoles d'authentification.

**Points clés :**
*   **Réplication automatisée en temps réel :** Synchronisation constante des machines virtuelles pour minimiser les fenêtres de perte de données en cas de sinistre ou d'attaque.
*   **Support étendu des hyperviseurs :** Compatibilité totale avec **VMware vSphere 9** (y compris vCenter, ESXi et VDDK 9.0.1.0) et **Proxmox VE 9.0/9.1**.
*   **Gestion Multi-tenant :** Amélioration de l'outil *MSP Direct Connect* pour une meilleure administration centralisée des environnements complexes.
*   **Mise à jour technologique :** Passage à Java SE 24 et intégration du framework Spring mis à jour pour améliorer la stabilité et les performances globales.

**Vulnérabilités traitées :**
*   **Obsolescence de l'authentification :** L'article souligne la fin de vie de l'authentification "Basic" par les fournisseurs majeurs (Google, Microsoft). NAKIVO remplace cette méthode par **OAuth 2.0** pour les notifications par e-mail, éliminant le stockage de mots de passe en clair. *Note : Aucune CVE spécifique n'est mentionnée, il s'agit d'une mesure proactive de sécurité liée aux standards d'authentification.*

**Recommandations :**
*   **Migrer vers OAuth 2.0 :** Configurer les notifications e-mail via le nouveau protocole OAuth 2.0 pour se conformer aux exigences de sécurité actuelles.
*   **Renforcer la défense contre les ransomwares :** Utiliser les capacités d'immuabilité sur les cibles S3/stockage objet et activer le scan anti-malware avant toute restauration.
*   **Maintenir l'isolation :** Exploiter les options de sauvegarde "air-gapped" (bandes, périphériques détachés, NAS hors ligne) comme ultime rempart contre les attaques par chiffrement.
*   **Mise à jour d'infrastructure :** Effectuer la montée de version vers la v11.2 pour bénéficier des correctifs de sécurité intégrés et de la prise en charge native des versions récentes de vSphere et Proxmox.

---
[Source](https://www.bleepingcomputer.com/news/security/nakivo-v112-ransomware-defense-faster-replication-vsphere-9-and-proxmox-ve-90-support/){:target="_blank"}
