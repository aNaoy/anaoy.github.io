---
title: '900+ Sangoma FreePBX Instances Compromised in Ongoing Web Shell Attacks'
date: 2026-02-27
permalink: /posts/2026/02/27/900-sangoma-freepbx-instances-compromised-in-ongoing-web-shell-attacks/
tags:
- veille-cyber
- hackernews
---
### Attaques en cours contre les instances Sangoma FreePBX

Plus de 900 instances de Sangoma FreePBX ont été compromises par des attaques exploitant une vulnérabilité d'injection de commandes. Les États-Unis comptent le plus grand nombre d'instances affectées, suivis par le Brésil, le Canada, l'Allemagne et la France.

**Points clés :**

*   Plus de 900 instances Sangoma FreePBX sont infectées par des web shells.
*   Ces attaques ont débuté en décembre 2025.
*   La vulnérabilité permet l'exécution de commandes arbitraires avec les privilèges de l'utilisateur "asterisk".
*   L'acteur de menace est identifié sous le nom d'INJ3CTOR3 et utilise le web shell EncystPHP.

**Vulnérabilité :**

*   **CVE-2025-64328** (score CVSS : 8.6) : Une faille de sécurité de haute gravité permettant l'injection de commandes après authentification.
*   **Versions affectées :** FreePBX versions 17.0.2.36 et antérieures.
*   **Correction :** La vulnérabilité a été corrigée dans la version 17.0.3.

**Recommandations :**

*   Mettre à jour les déploiements FreePBX vers la dernière version dès que possible.
*   Ajouter des contrôles de sécurité pour s'assurer que seuls les utilisateurs autorisés accèdent au panneau d'administration FreePBX (ACP).
*   Restreindre l'accès à l'ACP depuis des réseaux non fiables.
*   Mettre à jour le module "filestore" vers la dernière version.

---
[Source](https://thehackernews.com/2026/02/900-sangoma-freepbx-instances.html){:target="_blank"}
