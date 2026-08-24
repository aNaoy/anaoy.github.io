---
title: 'ReliaQuest confirms failed data-theft attack after ShinyHunters breach'
date: 2026-08-24
permalink: /posts/2026/08/24/reliaquest-confirms-failed-data-theft-attack-after-shinyhunters-breach/
tags:
- veille-cyber
- bleepingcomp
---
### Tentative d'intrusion ciblée chez ReliaQuest par le groupe ShinyHunters

La société de cybersécurité ReliaQuest a été la cible d'une campagne d'ingénierie sociale orchestrée par le groupe d'extorsion ShinyHunters. Bien que les attaquants aient réussi à compromettre les identifiants d'un employé, les mesures de sécurité interne ont empêché toute exfiltration de données ou accès aux systèmes critiques.

**Points clés :**
*   **Méthode d'attaque :** Utilisation de domaines frauduleux (ex: `reliaquest.claims`) et usurpation d'identité (vishing) pour tromper les employés.
*   **Accès limité :** Un employé a divulgué ses identifiants sur une fausse page SSO et validé une notification MFA, octroyant aux attaquants un accès restreint en "lecture seule" au tableau de bord d'identité.
*   **Défense efficace :** Les contrôles de confiance des périphériques (*device-trust controls*) ont bloqué toutes les tentatives ultérieures d'accès aux applications métier.
*   **Réponse :** ReliaQuest a révoqué les sessions, réinitialisé les mots de passe et les jetons d'authentification, confirmant l'absence de persistance ou de fuite de données.

**Vulnérabilités :**
*   **Ingénierie sociale (Vishing) :** Manipulation humaine réussie pour contourner les protections d'authentification initiale.
*   **Phishing MFA :** La validation d'une notification push sur un site frauduleux constitue le vecteur d'accès initial (aucune CVE spécifique n'est associée, il s'agit d'un risque inhérent aux processus d'authentification).

**Recommandations :**
*   **Renforcement du MFA :** Privilégier des méthodes d'authentification multifacteur résistantes au phishing (comme les clés de sécurité FIDO2/WebAuthn) plutôt que les notifications push classiques.
*   **Contrôles de confiance des terminaux :** Maintenir des politiques strictes de "device trust" pour limiter l'accès aux applications uniquement aux appareils gérés et conformes.
*   **Sensibilisation :** Former activement les employés aux techniques d'usurpation d'identité et à la vigilance face aux domaines suspects imitant l'infrastructure de l'entreprise.

---
[Source](https://www.bleepingcomputer.com/news/security/reliaquest-confirms-failed-data-theft-attack-after-shinyhunters-breach/){:target="_blank"}
