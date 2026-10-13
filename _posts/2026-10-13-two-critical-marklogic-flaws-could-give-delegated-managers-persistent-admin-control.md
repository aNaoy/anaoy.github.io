---
title: 'Two Critical MarkLogic Flaws Could Give Delegated Managers Persistent Admin Control'
date: 2026-10-13
permalink: /posts/2026/10/13/two-critical-marklogic-flaws-could-give-delegated-managers-persistent-admin-control/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques et correctifs majeurs dans MarkLogic Server

Progress Software a dévoilé 31 vulnérabilités affectant sa base de données MarkLogic Server, dont cinq sont classées comme critiques. Ces failles permettent principalement à des utilisateurs disposant de privilèges limités d'élever leurs droits pour obtenir un contrôle administrateur persistant sur le serveur.

**Points clés :**
*   **Gravité :** Plusieurs vulnérabilités présentent des scores CVSS de 9,9/10.
*   **Vecteur d'attaque :** La plupart des failles critiques nécessitent une authentification préalable (privilèges délégués) ou la capacité d'exécuter du code sur le serveur.
*   **Risques étendus :** Les vulnérabilités concernent divers composants, notamment les configurations SAML, OAuth, Kerberos, les environnements cloud (Azure/AWS) et les logs de diagnostic.
*   **Impact opérationnel :** La mise à jour apporte des changements de comportement significatifs (suppression de fonctionnalités obsolètes, nouvelles exigences de privilèges, limitations des outils comme *mlcp*), pouvant entraîner des incompatibilités avec les environnements existants.

**Vulnérabilités majeures (CVE) :**
*   **CVE-2026-85947 :** Abus des privilèges de gestion de "forest" pour créer un compte administrateur persistant.
*   **CVE-2026-85948 :** Injection XQuery dans une API obsolète permettant une prise de contrôle administrative.
*   **CVE-2026-85955 :** Exécution de code serveur avec des privilèges élevés via un abus des droits `xdmp-eval-in`.
*   **CVE-2026-85956 :** Accès non autorisé à des données critiques via la manipulation de backups/restaurations de "forests".
*   **CVE-2026-9191 :** Compromission d'une session authentifiée via des chemins d'évaluation REST/XDBC.

**Recommandations :**
*   **Mise à jour immédiate :** Passer à la version **11.3.7** (pour la branche LTS 11.x) ou **12.1.0** (pour la branche 12.x).
*   **Audit de sécurité :** Passer en revue les attributions de privilèges délégués (forest, base de données, `xdmp-eval-in`) avant et après la mise à jour.
*   **Vérification de configuration :** Désactiver les fonctionnalités obsolètes (OpsDirector, InfoStudio) et auditer les permissions des logs (`ErrorLog.txt`, `AuditLog.txt`).
*   **Consultation technique :** Étudier attentivement les notes de version concernant les incompatibilités (notamment pour l'outil *mlcp*) avant de déployer les correctifs, car des changements de sécurité par défaut pourraient bloquer les automatisations existantes.

---
[Source](https://thehackernews.com/2026/10/two-critical-marklogic-flaws-could-give.html){:target="_blank"}
