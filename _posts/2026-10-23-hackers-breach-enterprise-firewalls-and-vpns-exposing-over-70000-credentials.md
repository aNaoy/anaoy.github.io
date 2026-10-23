---
title: 'Hackers Breach Enterprise Firewalls and VPNs, Exposing Over 70,000 Credentials'
date: 2026-10-23
permalink: /posts/2026/10/23/hackers-breach-enterprise-firewalls-and-vpns-exposing-over-70000-credentials/
tags:
- veille-cyber
- hackernews
---
### Campagne massive de compromission d'équipements réseau par l'acteur "k0t"

Une vaste campagne cybercriminelle, attribuée à l'acteur de menace « k0t », cible les équipements de périphérie (firewalls et VPN) exposés sur Internet, tels que Fortinet FortiGate et Palo Alto Networks GlobalProtect. L'attaquant agit comme un courtier en accès initial, revendant ou exploitant des accès pour le compte de groupes de ransomware comme Qilin et The Gentlemen, ayant compromis plus de 70 000 identifiants.

**Points clés :**
*   **Méthodologie :** Utilisation massive de moteurs de recherche spécialisés (FOFA, ZoomEye) pour identifier les équipements vulnérables.
*   **Persistance :** Installation d'outils d'administration légitimes (MeshCentral, Atera, AnyDesk) et du framework AdaptixC2.
*   **Exfiltration :** Utilisation de l'outil Rclone pour transférer les données volées vers des stockages cloud (Wasabi S3, MEGA).
*   **Ciblage :** Approche opportuniste mondiale, avec une forte concentration en Asie-Pacifique et Amérique latine.

**Vulnérabilités exploitées :**
*   **CVE-2025-64446 :** Faille de traversée de chemin (*path traversal*) dans FortiWeb.
*   **CVE-2026-0257 :** Faille de contournement d'authentification dans Palo Alto Networks PAN-OS et Prisma Access.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer sans délai les correctifs de sécurité pour les vulnérabilités citées.
*   **Réduction de la surface d'attaque :** Restreindre l'exposition directe des interfaces de gestion des VPN et firewalls sur Internet.
*   **Audit d'accès :** Surveiller les connexions VPN (notamment OpenConnect) et identifier toute présence d'outils d'administration à distance non autorisés.
*   **Gestion des identifiants :** Procéder à une rotation des mots de passe pour les comptes exposés et auditer les annuaires LDAP/Active Directory à la recherche d'activités suspectes.

---
[Source](https://thehackernews.com/2026/10/hackers-breach-enterprise-firewalls-and.html){:target="_blank"}
