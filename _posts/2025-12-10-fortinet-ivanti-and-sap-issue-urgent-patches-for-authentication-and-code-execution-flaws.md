---
title: 'Fortinet, Ivanti, and SAP Issue Urgent Patches for Authentication and Code Execution Flaws'
date: 2025-12-10
permalink: /posts/2025/12/10/fortinet-ivanti-and-sap-issue-urgent-patches-for-authentication-and-code-execution-flaws/
tags:
- veille-cyber
- hackernews
---
**Alertes Urgentes pour Failles de Sécurité Fortinet, Ivanti et SAP**

Des vulnérabilités critiques ont été identifiées dans les produits de Fortinet, Ivanti et SAP, potentiellement exploitables pour contourner l'authentification et exécuter du code malveillant.

**Points Clés :**

*   **Fortinet :** Des vulnérabilités (CVE-2025-59718, CVE-2025-59719, score CVSS 9.8) affectent FortiOS, FortiWeb, FortiProxy et FortiSwitchManager. Elles concernent une mauvaise vérification de signature cryptographique, permettant à un attaquant non authentifié de contourner l'authentification SSO FortiCloud via un message SAML falsifié, si cette fonctionnalité est activée. Par défaut, cette fonctionnalité n'est pas activée.
*   **Ivanti :** Quatre failles ont été corrigées dans Endpoint Manager (EPM). La plus critique (CVE-2025-10573, score CVSS 9.6) est une faille XSS stockée dans le cœur et les consoles distantes d'EPM. Un attaquant non authentifié peut exécuter du JavaScript arbitraire dans le contexte d'une session administrateur en intégrant du JavaScript malveillant dans le tableau de bord administrateur. L'exploitation nécessite une interaction utilisateur (visualisation du tableau de bord). Trois autres vulnérabilités graves (CVE-2025-13659, CVE-2025-13661, CVE-2025-13662) permettent l'exécution de code à distance, la CVE-2025-13662 étant liée à une mauvaise vérification de signature cryptographique dans le composant de gestion des correctifs.
*   **SAP :** Trois vulnérabilités critiques ont été corrigées parmi 14 failles dans divers produits. Il s'agit de CVE-2025-42880 (score CVSS 9.9) pour une injection de code dans SAP Solution Manager, CVE-2025-55754 (score CVSS 9.6) pour de multiples vulnérabilités dans Apache Tomcat au sein de SAP Commerce Cloud, et CVE-2025-42928 (score CVSS 9.1) pour une vulnérabilité de désérialisation dans SAP jConnect SDK pour Sybase Adaptive Server Enterprise (ASE), qui requiert des privilèges élevés pour être exploitée.

**Vulnérabilités :**

*   **Fortinet :**
    *   CVE-2025-59718
    *   CVE-2025-59719
*   **Ivanti :**
    *   CVE-2025-10573
    *   CVE-2025-13659
    *   CVE-2025-13661
    *   CVE-2025-13662
*   **SAP :**
    *   CVE-2025-42880
    *   CVE-2025-55754
    *   CVE-2025-42928

**Recommandations :**

*   **Fortinet :** Désactiver temporairement la fonctionnalité de connexion FortiCloud SSO si elle est activée, ou appliquer les correctifs dès que possible.
*   **Ivanti :** Appliquer la mise à jour EPM version 2024 SU4 SR1.
*   **SAP :** Appliquer les mises à jour de sécurité de décembre pour les produits concernés, en particulier pour SAP Solution Manager.

Il est crucial d'appliquer rapidement ces correctifs pour se prémunir contre les risques d'exploitation par des acteurs malveillants.

---
[Source](https://thehackernews.com/2025/12/fortinet-ivanti-and-sap-issue-urgent.html){:target="_blank"}
