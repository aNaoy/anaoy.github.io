---
title: 'European Commission investigating breach after Amazon cloud account hack'
date: 2026-03-27
permalink: /posts/2026/03/27/european-commission-investigating-breach-after-amazon-cloud-account-hack/
tags:
- veille-cyber
- bleepingcomp
---
### Cyberattaque contre l'infrastructure cloud de la Commission européenne

La Commission européenne mène actuellement une enquête suite à une intrusion dans son environnement Amazon Web Services (AWS). Un pirate informatique affirme avoir exfiltré plus de 350 Go de données, incluant des bases de données et des informations relatives au personnel, avec l'intention de les publier en ligne. AWS a précisé que ses propres services ne sont pas en cause, l'incident étant limité au compte spécifique de la Commission.

**Points clés :**
*   **Nature de l'incident :** Accès non autorisé au compte AWS de la Commission européenne.
*   **Données impactées :** Environ 350 Go de données volées, incluant des informations sur les employés et accès à un serveur mail.
*   **Contexte :** Il s'agit du second incident majeur pour l'institution cette année, faisant suite à une faille exploitée sur sa plateforme de gestion d'appareils mobiles en février.
*   **Position de l'attaquant :** L'auteur revendique l'accès sans demande de rançon, privilégiant la divulgation publique des données.

**Vulnérabilités :**
*   Bien que le vecteur d'accès pour cette intrusion AWS ne soit pas encore divulgué, les précédents incidents récents au sein des institutions européennes ont été liés à des vulnérabilités d'injection de code dans le logiciel **Ivanti Endpoint Manager Mobile (EPMM)**.

**Recommandations :**
*   **Renforcement des accès :** Imposer une authentification multifacteur (MFA) robuste sur tous les comptes cloud et services tiers.
*   **Gestion des correctifs :** Appliquer immédiatement les mises à jour de sécurité pour les solutions logicielles exposées (notamment Ivanti EPMM).
*   **Surveillance proactive :** Renforcer la détection des activités anormales au sein des environnements cloud pour identifier rapidement les accès non autorisés.
*   **Audit des privilèges :** Appliquer le principe du moindre privilège pour limiter l'impact potentiel en cas de compromission d'un compte utilisateur.

---
[Source](https://www.bleepingcomputer.com/news/security/european-commission-investigating-breach-after-amazon-cloud-account-hack/){:target="_blank"}
