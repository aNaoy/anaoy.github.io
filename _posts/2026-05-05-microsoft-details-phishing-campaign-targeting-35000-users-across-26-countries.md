---
title: 'Microsoft Details Phishing Campaign Targeting 35,000 Users Across 26 Countries'
date: 2026-05-05
permalink: /posts/2026/05/05/microsoft-details-phishing-campaign-targeting-35000-users-across-26-countries/
tags:
- veille-cyber
- hackernews
---
### Campagne mondiale de phishing et menaces émergentes en 2026

Microsoft a identifié une vaste campagne de vol d'identifiants ciblant 35 000 utilisateurs dans 26 pays, principalement dans les secteurs de la santé, de la finance et de la technologie. Utilisant des thématiques de conformité interne (« Code of Conduct »), les attaquants envoient des emails légitimes contenant des pièces jointes PDF. Ces messages redirigent les victimes vers des pages de phishing protégées par des CAPTCHA pour contourner l'analyse automatisée, aboutissant à une attaque de type *Adversary-in-the-Middle* (AiTM) permettant de dérober les jetons d'authentification et de contourner le MFA.

**Points clés :**
* **Méthodologie :** Usage de modèles HTML professionnels, de services d'envoi d'emails légitimes et de plateformes de phishing-as-a-service (PhaaS) comme Tycoon 2FA, Kratos et EvilTokens.
* **Évolution des menaces :** Forte augmentation du phishing par QR code (+146 % au T1 2026) et usage détourné d'Amazon SES (via des clés AWS compromises) pour contourner les contrôles SPF, DKIM et DMARC.
* **Volume :** Plus de 8 milliards de menaces par email détectées au premier trimestre 2026, avec une prédominance du vol d'identifiants sur la distribution de malwares.

**Vulnérabilités exploitées :**
* **Facteur humain :** Exploitation de l'urgence et de la confiance envers les communications internes.
* **Faiblesse d'infrastructure :** Abus des clés d'accès AWS pour détourner le service Amazon SES (non liée à une CVE spécifique, mais à une mauvaise gestion des secrets/clés).
* **Contournement MFA :** Utilisation de techniques AiTM pour intercepter les sessions actives en temps réel.

**Recommandations :**
* **Authentification renforcée :** Privilégier les méthodes de connexion résistantes au phishing, telles que les clés de sécurité physiques (FIDO2/WebAuthn).
* **Sécurité des accès :** Protéger rigoureusement les clés d'accès (AWS Access Keys) et mettre en place une rotation fréquente des identifiants API.
* **Formation :** Sensibiliser les employés à la méfiance envers les demandes d'action urgentes ou les notifications de "non-conformité" reçues par email, même si le message semble provenir de sources internes authentifiées.
* **Filtrage avancé :** Renforcer les défenses contre le phishing par QR code et les redirections CAPTCHA suspectes dans les passerelles de messagerie.

---
[Source](https://thehackernews.com/2026/05/microsoft-details-phishing-campaign.html){:target="_blank"}
