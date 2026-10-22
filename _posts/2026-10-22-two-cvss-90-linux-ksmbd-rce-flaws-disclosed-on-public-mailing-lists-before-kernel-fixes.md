---
title: 'Two CVSS 9.0 Linux KSMBD RCE Flaws Disclosed on Public Mailing Lists Before Kernel Fixes'
date: 2026-10-22
permalink: /posts/2026/10/22/two-cvss-90-linux-ksmbd-rce-flaws-disclosed-on-public-mailing-lists-before-kernel-fixes/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques d'exécution de code à distance dans KSMBD Linux

Deux vulnérabilités critiques de type exécution de code à distance (RCE) affectant KSMBD, le serveur SMB intégré au noyau Linux, ont été divulguées publiquement via des listes de diffusion. Bien qu'elles affichent un score CVSS de 9.0, aucun correctif officiel n'est actuellement disponible dans le noyau principal.

**Points clés :**
* **Nature des failles :** Les vulnérabilités permettent une exécution de code à distance sans nécessiter de correctif immédiat disponible.
* **Absence de CVE :** Le projet Linux n'attribue de CVE qu'une fois qu'un correctif est validé dans une branche stable.
* **Contexte de divulgation :** Les rapports ont été transmis publiquement par Trend Micro (via leur outil d'IA) sans correctif associé, ce qui a suscité des critiques de la part des mainteneurs du noyau.

**Vulnérabilités identifiées :**
* **ZDI-CAN-33549 :** Dépassement d'entier (integer underflow) dans le chemin SMB Direct. Nécessite une interface réseau compatible RDMA, une lecture/écriture sur un partage KSMBD et la négociation SMB Direct.
* **ZDI-CAN-33774 :** Erreur de traitement (race condition) dans la table de gestion KSMBD. Cette faille ne nécessite aucune authentification et expose tout serveur utilisant KSMBD sur le port 445.

**Recommandations :**
* **Vérification :** Déterminer si le module KSMBD est actif sur vos systèmes via les commandes `systemctl status ksmbd` ou `lsmod | grep ksmbd`.
* **Surveillance :** Garder une vigilance accrue sur les mises à jour du noyau et les annonces de sécurité de votre distribution Linux.
* **Réduction de la surface d'attaque :** En l'absence de correctif, envisager de désactiver le service KSMBD si celui-ci n'est pas strictement nécessaire, ou isoler les serveurs exposés via des pare-feux stricts.

---
[Source](https://thehackernews.com/2026/10/two-cvss-90-linux-ksmbd-rce-flaws.html){:target="_blank"}
