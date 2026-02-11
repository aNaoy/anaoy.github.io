---
title: 'Over 60 Software Vendors Issue Security Fixes Across OS, Cloud, and Network Platforms'
date: 2026-02-11
permalink: /posts/2026/02/11/over-60-software-vendors-issue-security-fixes-across-os-cloud-and-network-platforms/
tags:
- veille-cyber
- hackernews
---
**Vague de Corrections de Sécurité Logicielle : Plus de 60 Fournisseurs Agissent**

Un nombre important de fournisseurs de logiciels ont publié des correctifs pour diverses vulnérabilités de sécurité affectant leurs produits et services. Cette initiative, souvent liée au "Patch Tuesday", couvre un large éventail de plateformes, y compris les systèmes d'exploitation, le cloud et les infrastructures réseau.

Parmi les mises à jour notables :

*   **Microsoft** a corrigé 59 failles, dont six vulnérabilités zero-day exploitées activement dans divers composants Windows. Ces failles permettaient de contourner des mesures de sécurité, d'escalader des privilèges ou de provoquer des dénis de service.
*   **Adobe** a publié des misesStudiot pour plusieurs de ses logiciels créatifs, tels qu'Audition et After Effects. Aucune exploitation active n'a été signalée.
*   **SAP** a résolu deux vulnérabilités critiques :
    *   Une injection de code dans SAP CRM et SAP S/4HANA (CVE-2026-0488, score CVSS 9.9) permettant une compromission complète de la base de données.
    *   Une absence de vérification d'autorisation dans SAP NetWeaver Application Server ABAP et ABAP Platform (CVE-2026-0509, score CVSS 9.6), permettant à un utilisateur authentifié de bas privilège d'exécuter des appels de fonctions à distance sans autorisation adéquate.
*   **Intel** et **Google** ont conjointement examiné la sécurité des extensions de domaine de confiance (TDX) 1.5 d'Intel, découvrant cinq vulnérabilités (CVE-2025-32007, CVE-2025-27940, CVE-2025-30513, CVE-2025-27572, et CVE-2025-32467) et de nombreuses autres faiblesses.

La liste complète des fournisseurs ayant publié des mises à jour de sécurité comprend également ABB, AWS, AMD, Apple, ASUS, Cisco, Dell, Fortinet, Google (Android, Chrome, Cloud), HP, IBM, Intel, Lenovo, divers distributions Linux (Debian, Red Hat, Ubuntu, etc.), Microsoft, Mozilla (Firefox, Thunderbird), NVIDIA, Oracle, SAP, Siemens, VMware, et bien d'autres.

**Points Clés :**

*   Large mise à jour de sécurité couvrant de nombreux fournisseurs.
*   Correction de vulnérabilités critiques, y compris des zero-days exploitées activement.
*   Focus sur les systèmes d'exploitation, les applications cloud et les infrastructures réseau.

**Vulnérabilités (avec CVE si disponibles) :**

*   **Microsoft Windows** : Six zero-days exploitées activement pour contournement de sécurité, escalade de privilèges et déni de service (détails non spécifiés dans l'article).
*   **SAP CRM / S/4HANA** : Injection de code (CVE-2026-0488, CVSS 9.9).
*   **SAP NetWeaver AS ABAP / ABAP Platform** : Absence de vérification d'autorisation (CVE-2026-0509, CVSS 9.6).
*   **Intel TDX 1.5** : CVE-2025-32007, CVE-2025-27940, CVE-2025-30513, CVE-2025-27572, CVE-2025-32467.

**Recommandations :**

*   **Appliquer les correctifs de sécurité** dès que possible pour les produits et services affectés.
*   Pour SAP, une mise à jour du noyau et une configuration du paramètre de profil sont nécessaires pour corriger les vulnérabilités, avec des ajustements potentiels des rôles utilisateurs et des paramètres UCON.

---
[Source](https://thehackernews.com/2026/02/over-60-software-vendors-issue-security.html){:target="_blank"}
