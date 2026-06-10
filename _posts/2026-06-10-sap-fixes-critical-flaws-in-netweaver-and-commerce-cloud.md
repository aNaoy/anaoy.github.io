---
title: 'SAP fixes critical flaws in NetWeaver and Commerce Cloud'
date: 2026-06-10
permalink: /posts/2026/06/10/sap-fixes-critical-flaws-in-netweaver-and-commerce-cloud/
tags:
- veille-cyber
- bleepingcomp
---
### Correctifs de sécurité critiques pour SAP NetWeaver et Commerce Cloud

SAP a publié son bulletin de sécurité de juin 2026, corrigeant 15 vulnérabilités, dont quatre failles critiques affectant ses plateformes principales, NetWeaver et Commerce Cloud. Ces défauts exposent les entreprises à des risques d'usurpation d'identité, de corruption mémoire et d'accès non autorisés.

**Points clés :**
*   **Produits impactés :** SAP NetWeaver (AS ABAP et Java) et SAP Commerce Cloud.
*   **Nature des risques :** Les vulnérabilités permettent des contournements d'authentification, des corruptions de mémoire et des manipulations de répertoires.
*   **Vulnérabilités critiques identifiées :**
    *   **CVE-2026-44748 (CVSS 9.9) :** Attaque par "XML Signature Wrapping" dans NetWeaver AS ABAP, permettant de contourner l'authentification SAML.
    *   **CVE-2026-27671 (CVSS 9.8) :** Corruption de mémoire dans le serveur d'application ABAP, exploitable sans authentification via des requêtes RFC malveillantes.
    *   **CVE-2026-22732 (CVSS 9.1) :** Faille liée à Spring Security affectant SAP Commerce Cloud et Data Hub.
    *   **CVE-2026-40128 (CVSS 9.0) :** Traversée de répertoire (directory traversal) dans le conteneur Web de NetWeaver AS Java.

**Recommandations :**
*   **Priorisation :** Appliquer immédiatement les correctifs, en se concentrant en priorité sur les CVE-2026-44748 et CVE-2026-27671 en raison de leur sévérité extrême.
*   **Accès aux correctifs :** Les clients SAP doivent consulter le portail de sécurité officiel de SAP pour obtenir les détails techniques complets et les instructions de mise à jour spécifiques à leurs environnements.

---
[Source](https://www.bleepingcomputer.com/news/security/sap-fixes-critical-flaws-in-netweaver-and-commerce-cloud/){:target="_blank"}
