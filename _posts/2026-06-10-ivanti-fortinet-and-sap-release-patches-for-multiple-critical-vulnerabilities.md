---
title: 'Ivanti, Fortinet, and SAP Release Patches for Multiple Critical Vulnerabilities'
date: 2026-06-10
permalink: /posts/2026/06/10/ivanti-fortinet-and-sap-release-patches-for-multiple-critical-vulnerabilities/
tags:
- veille-cyber
- hackernews
---
### Alertes de sécurité critiques : Correctifs pour Fortinet, Ivanti et SAP

Les éditeurs Fortinet, Ivanti et SAP ont publié des mises à jour correctives pour plusieurs vulnérabilités critiques permettant l'exécution de code arbitraire et l'accès non autorisé à des données sensibles. Aucune exploitation active n'a été signalée à ce jour.

**Points clés et vulnérabilités :**

*   **Fortinet (FortiSandbox) :**
    *   **CVE-2026-25089** (Score CVSS 9.1) : Injection de commande OS via l'interface web, permettant à un attaquant non authentifié d'exécuter des commandes via des requêtes HTTP contrefaites.
*   **Ivanti (Sentry/MobileIron Sentry) :**
    *   **CVE-2026-10520** (Score CVSS 10.0) : Injection de commande OS permettant une exécution de code à distance avec les privilèges root.
    *   **CVE-2026-10523** (Score CVSS 9.9) : Contournement d'authentification permettant la création de comptes administrateurs arbitraires.
*   **SAP (NetWeaver, ABAP, Commerce Cloud, Data Hub) :**
    *   **CVE-2026-44748** (Score CVSS 9.9) : Vulnérabilité d'enveloppement de signature XML dans l'authentification SAML.
    *   **CVE-2026-27671** (Score CVSS 9.8) : Corruption mémoire dans le serveur d'application ABAP via des requêtes RFC.
    *   **CVE-2026-22732** (Score CVSS 9.1) : Vulnérabilité liée à Spring Security.
    *   **CVE-2026-40128** (Score CVSS 9.0) : Traversée de répertoire dans le conteneur web Java de SAP NetWeaver.

**Recommandations :**

*   **Application immédiate des correctifs :** Il est impératif de mettre à jour les solutions concernées vers les dernières versions disponibles fournies par les éditeurs.
*   **Ivanti :** Les versions antérieures à R10.5.2, R10.6.2 et R10.7.1 doivent être mises à jour pour bloquer l'accès aux points de terminaison vulnérables.
*   **Fortinet :** Les instances de FortiSandbox doivent être mises à jour vers les versions 5.0.6 (ou 4.4.9 pour les branches 4.x) a minima.
*   **Veille :** Consulter les bulletins de sécurité spécifiques de chaque fournisseur (FortiGuard, Ivanti Hub et SAP Security Notes) pour obtenir les détails techniques complets et les procédures de déploiement.

---
[Source](https://thehackernews.com/2026/06/ivanti-fortinet-and-sap-release-patches.html){:target="_blank"}
