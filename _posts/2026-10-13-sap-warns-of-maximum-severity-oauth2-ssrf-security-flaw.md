---
title: 'SAP warns of maximum severity OAuth2 SSRF security flaw'
date: 2026-10-13
permalink: /posts/2026/10/13/sap-warns-of-maximum-severity-oauth2-ssrf-security-flaw/
tags:
- veille-cyber
- bleepingcomp
---
### Alertes de sécurité SAP : correctifs critiques d'octobre 2026

SAP a publié ses mises à jour de sécurité d'octobre 2026, corrigeant 20 vulnérabilités affectant divers produits de son écosystème.

**Points clés**
*   Le correctif le plus critique concerne une faille SSRF (Server-Side Request Forgery) dans le **Cloud SDK for Python**, permettant le vol d'identifiants OAuth2.
*   D'autres failles critiques ont été corrigées dans **SAP NetWeaver Visual Composer** et **SAP Manufacturing Integration and Intelligence**, pouvant mener à une compromission totale du système.
*   La CISA maintient une vigilance accrue sur les vulnérabilités SAP, ayant déjà identifié 14 failles exploitées activement dans le passé, dont certaines liées à des attaques par ransomware.

**Vulnérabilités majeures**
*   **CVE-2026-89111** : Vulnérabilité SSRF OAuth2 dans le Cloud SDK for Python, exploitable à distance sans privilèges pour exfiltrer des identifiants.
*   **CVE-2026-89110** : Faille critique de contrôle d'accès dans SAP NetWeaver Visual Composer.
*   **CVE-2026-89108** : Faille critique dans SAP Manufacturing Integration and Intelligence permettant une élévation de privilèges.

**Recommandations**
*   **Appliquer les correctifs** : Déployer sans délai les mises à jour de sécurité d'octobre 2026 fournies par SAP.
*   **Atténuation temporaire (CVE-2026-89111)** : Pour les applications multi-tenant ne pouvant être patchées immédiatement, mettre en place une liste blanche (allowlist) validant les valeurs du paramètre `tenant_subdomain` avant tout appel au SDK.

---
[Source](https://www.bleepingcomputer.com/news/security/sap-warns-of-maximum-severity-oauth2-ssrf-security-flaw/){:target="_blank"}
