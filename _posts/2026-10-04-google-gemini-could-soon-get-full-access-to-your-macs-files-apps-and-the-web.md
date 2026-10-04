---
title: 'Google Gemini could soon get full access to your Mac’s files, apps and the web'
date: 2026-10-04
permalink: /posts/2026/10/04/google-gemini-could-soon-get-full-access-to-your-macs-files-apps-and-the-web/
tags:
- veille-cyber
- bleepingcomp
---
### Vers une intégration profonde de Google Gemini sur macOS : risques et contrôle

Google développe une nouvelle fonctionnalité pour l'application Gemini sur macOS permettant à l'IA d'accéder aux fichiers locaux, de naviguer sur le web et d'interagir directement avec des applications natives (Mail, Safari, Messages). Une option en phase de test, nommée « Additional sandbox options », permettrait à l'IA d'effectuer des actions sans demande d'autorisation systématique.

**Points clés :**
*   **Accès étendu :** Gemini pourrait lire, créer, modifier ou supprimer des fichiers sur l'ensemble du système, dépassant le cadre des dossiers partagés initialement.
*   **Automatisation :** L'IA est conçue pour réaliser des tâches complexes à travers les applications installées sur le Mac.
*   **Gardes-fous :** Google prévoit de maintenir une validation humaine obligatoire pour les actions critiques (achats, virements, création de comptes, modifications de données sensibles).
*   **Conflit potentiel :** Apple étudie des restrictions visant à limiter l'accès des agents IA aux données personnelles sur macOS.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée, car il s'agit d'une fonctionnalité expérimentale.
*   Risque d'escalade de privilèges : permettre à une IA de modifier des fichiers en dehors d'une zone isolée (« sandbox ») expose le système à des risques de compromission si l'IA est induite en erreur (via des attaques par *prompt injection* par exemple).

**Recommandations :**
*   **Surveillance active :** Rester vigilant quant à l'activation des options de contrôle étendu (« sandbox options ») une fois la fonctionnalité déployée.
*   **Principe du moindre privilège :** Limiter les autorisations accordées aux applications d'IA lorsque le système d'exploitation offre des réglages granulaires.
*   **Veille de sécurité :** Surveiller les futures mises à jour d'Apple concernant la gestion des permissions pour les agents IA sur macOS afin de bénéficier des protections natives du système.

---
[Source](https://www.bleepingcomputer.com/news/google/google-gemini-could-soon-get-full-access-to-your-macs-files-apps-and-the-web/){:target="_blank"}
