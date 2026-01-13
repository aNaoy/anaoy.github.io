---
title: 'ServiceNow Patches Critical AI Platform Flaw Allowing Unauthenticated User Impersonation'
date: 2026-01-13
permalink: /posts/2026/01/13/servicenow-patches-critical-ai-platform-flaw-allowing-unauthenticated-user-impersonation/
tags:
- veille-cyber
- hackernews
---
**Vulnérabilité Majeure dans la Plateforme IA de ServiceNow Corrigée**

Une faille de sécurité critique affectant la plateforme d'intelligence artificielle de ServiceNow a été corrigée. Cette vulnérabilité permettait à un utilisateur non authentifié de se faire passer pour un autre utilisateur et d'effectuer des actions arbitraires en son nom.

**Points Clés :**

*   **Impact :** Possibilité d'usurpation d'identité d'utilisateurs, y compris des administrateurs, sans authentification.
*   **Exploitation :** Bypass des mécanismes d'authentification multi-facteurs (MFA) et d'authentification unique (SSO).
*   **Conséquences Potentielles :** Exécution d'actions non autorisées, vol de données sensibles, modification d'enregistrements, création de comptes avec des privilèges élevés, et manipulation des outils IA de l'entreprise.
*   **Découverte :** Signalée par Aaron Costello d'AppOmni en octobre 2025.
*   **Correction :** ServiceNow a déployé une mise à jour de sécurité le 30 octobre 2025 pour la majorité des instances hébergées et a partagé les correctifs avec ses partenaires et clients utilisant des installations auto-hébergées.

**Vulnérabilités :**

*   **Nom :** BodySnatcher
*   **Référence CVE :** CVE-2025-12420
*   **Score CVSS :** 9.3/10.0

**Recommandations :**

*   Appliquer dès que possible la mise à jour de sécurité fournie par ServiceNow pour atténuer les menaces potentielles. Les versions corrigées incluent :
    *   Now Assist AI Agents (sn\_aia) : 5.1.18 ou ultérieure et 5.2.19 ou ultérieure
    *   Virtual Agent API (sn\_va\_as\_service) : 3.15.2 ou ultérieure et 4.0.4 ou ultérieure

---
[Source](https://thehackernews.com/2026/01/servicenow-patches-critical-ai-platform.html){:target="_blank"}
