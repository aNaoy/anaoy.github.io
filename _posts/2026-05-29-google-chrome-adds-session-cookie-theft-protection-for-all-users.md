---
title: 'Google Chrome adds session cookie theft protection for all users'
date: 2026-05-29
permalink: /posts/2026/05/29/google-chrome-adds-session-cookie-theft-protection-for-all-users/
tags:
- veille-cyber
- bleepingcomp
---
### Protection contre le vol de cookies avec DBSC dans Chrome

Google déploie désormais la fonctionnalité « Device Bound Session Credentials » (DBSC) pour l'ensemble des utilisateurs de Chrome. Cette mesure de sécurité vise à contrer le vol de cookies de session, une technique couramment utilisée par les logiciels malveillants (*infostealers*) pour contourner l'authentification multifacteur (MFA) et prendre le contrôle des comptes.

**Points clés :**
*   **Liaison matérielle :** DBSC lie cryptographiquement les cookies de session au matériel de l'utilisateur via une puce de sécurité (TPM sur Windows, Secure Enclave sur macOS).
*   **Prévention proactive :** Contrairement à la détection réactive, cette méthode rend les cookies exfiltrés inutilisables sur toute autre machine que celle d'origine, car les attaquants n'ont pas accès aux clés cryptographiques liées à la puce matérielle.
*   **Déploiement généralisé :** La fonctionnalité est activée par défaut pour tous les comptes Google (Workspace et personnels). Les administrateurs Workspace ne peuvent pas la désactiver.

**Vulnérabilités adressées :**
*   **Vol de cookies de session :** Le détournement de jetons d'authentification pour usurper l'identité d'un utilisateur.
*   **Abus de l'API Google OAuth « MultiLogin » :** Des malwares (comme *Lumma* ou *Rhadamanthys*) exploitaient cette API pour régénérer des cookies après expiration. DBSC neutralise cette méthode en invalidant l'utilisation des jetons volés.

**Recommandations :**
*   **Mise à jour :** S'assurer que le navigateur Google Chrome est à jour pour bénéficier de cette protection automatiquement.
*   **Sécurité renforcée :** Continuer d'utiliser le mode « Navigation sécurisée renforcée » (*Enhanced Safe Browsing*) dans Chrome pour une protection complémentaire contre le phishing et les logiciels malveillants.
*   **Hygiène numérique :** Bien que DBSC limite l'impact des cookies volés, il reste crucial de maintenir les appareils exempts de logiciels malveillants pour prévenir d'autres types d'atteintes à la vie privée.

---
[Source](https://www.bleepingcomputer.com/news/security/google-chrome-adds-session-cookie-theft-protection-for-all-users/){:target="_blank"}
