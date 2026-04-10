---
title: 'Google Rolls Out DBSC in Chrome 146 to Block Session Theft on Windows'
date: 2026-04-10
permalink: /posts/2026/04/10/google-rolls-out-dbsc-in-chrome-146-to-block-session-theft-on-windows/
tags:
- veille-cyber
- hackernews
---
### Protection contre le vol de session : Google déploie DBSC sur Chrome

Google a généralisé la technologie **Device Bound Session Credentials (DBSC)** pour les utilisateurs de Chrome sous Windows (version 146). Ce mécanisme vise à neutraliser le vol de jetons de session, une technique couramment exploitée par les logiciels malveillants de type « infostealer » (comme Lumma ou Vidar) pour accéder aux comptes sans mot de passe.

**Points clés :**
* **Liaison matérielle :** DBSC lie cryptographiquement une session de navigation à un appareil spécifique en utilisant des modules de sécurité matériels (TPM sur Windows, Secure Enclave sur macOS).
* **Rendre les cookies inutilisables :** Si un attaquant dérobe un cookie de session, celui-ci devient inexploitable car il est associé à une clé privée non exportable, présente uniquement sur la machine de la victime.
* **Confidentialité :** Le protocole est conçu pour empêcher le suivi inter-sites (tracking) ; aucun identifiant d'appareil n'est transmis au serveur.
* **Déploiement :** Actuellement disponible sur Windows, avec une extension prévue sur macOS dans une future mise à jour. En cas d'incompatibilité matérielle, le navigateur revient automatiquement au comportement standard.

**Vulnérabilités ciblées :**
* Le vol de cookies de session (session hijacking) via des logiciels malveillants (infostealers). Aucune CVE spécifique n'est mentionnée, car il s'agit d'une contre-mesure architecturale globale contre une famille de menaces plutôt que d'une correction de vulnérabilité logicielle isolée.

**Recommandations :**
* Mettre à jour Google Chrome vers la version 146 ou ultérieure pour bénéficier automatiquement de cette protection.
* Maintenir les systèmes à jour pour assurer la compatibilité avec les modules de sécurité matériels (TPM).

---
[Source](https://thehackernews.com/2026/04/google-rolls-out-dbsc-in-chrome-146-to.html){:target="_blank"}
