---
title: 'Europol-coordinated action disrupts Tycoon2FA phishing platform'
date: 2026-03-04
permalink: /posts/2026/03/04/europol-coordinated-action-disrupts-tycoon2fa-phishing-platform/
tags:
- veille-cyber
- bleepingcomp
---
### Démantèlement de la plateforme de phishing Tycoon2FA

Une opération policière internationale, coordonnée par Europol et soutenue par des partenaires privés comme Microsoft et Trend Micro, a neutralisé Tycoon2FA, une plateforme majeure de "phishing-as-a-service" (PhaaS). Cette opération a abouti à la saisie de 330 domaines utilisés par le service criminel, interrompant ainsi son activité qui générait des millions de messages de phishing mensuels.

Tycoon2FA, actif depuis août 2023, permettait aux cybercriminels de contourner les protections d'authentification multifacteur (MFA) et de compromettre les comptes d'environ 100 000 organisations mondiales, y compris des institutions gouvernementales, des écoles et des organisations de santé.

**Points clés :**

*   **Démantèlement d'une infrastructure majeure de phishing :** L'opération a perturbé Tycoon2FA, une plateforme de phishing à grande échelle.
*   **Impact mondial :** Des centaines de milliers d'organisations étaient ciblées.
*   **Coopération public-privé :** L'action a impliqué plusieurs agences de maintien de l'ordre et des entreprises de cybersécurité.

**Vulnérabilités exploitées :**

*   **Contournement de l'authentification multifacteur (MFA) :** Tycoon2FA utilisait une technique d'adversaire-dans-la-mêlée (AitM) pour intercepter les identifiants de connexion et les cookies de session des victimes en temps réel.
*   **Usurpation d'identité de services légitimes :** La plateforme imitait les pages de connexion de services populaires tels que Microsoft 365, OneDrive, Outlook, SharePoint et Gmail.
*   **Persistance et accès aux données :** Elle permettait aux attaquants de maintenir l'accès aux informations sensibles même après la réinitialisation des mots de passe, sauf si les sessions actives et les jetons étaient explicitement révoqués.

**Recommandations :**

Bien que l'article ne détaille pas de recommandations spécifiques de la part des forces de l'ordre suite à ce démantèlement, les attaques de type AitM soulignent l'importance de :

*   **Surveiller activement les sessions actives :** Les organisations devraient mettre en place des mécanismes pour détecter et révoquer les sessions suspectes, même si les identifiants semblent valides.
*   **Sensibilisation des utilisateurs :** Informer les employés sur les techniques de phishing avancées et la prudence à adopter face aux demandes d'informations d'identification.
*   **Utilisation de solutions de sécurité robustes :** S'appuyer sur des solutions capables de détecter les tentatives de phishing avancées et les manipulations de session.

---
[Source](https://www.bleepingcomputer.com/news/security/europol-coordinated-action-disrupts-tycoon2fa-phishing-platform/){:target="_blank"}
