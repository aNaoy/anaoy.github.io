---
title: 'Cisco Patches Nine Crosswork and Secure Workload Flaws, Five Scoring CVSS 10.0'
date: 2026-08-21
permalink: /posts/2026/08/21/cisco-patches-nine-crosswork-and-secure-workload-flaws-five-scoring-cvss-100/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans les solutions Cisco Crosswork et Secure Workload

Cisco a publié des correctifs de sécurité majeurs pour ses plateformes **Crosswork** et **Secure Workload**, suite à une revue interne approfondie. Bien qu'aucune exploitation active ne soit signalée, la criticité élevée de ces failles impose une mise à jour immédiate.

#### Points clés
*   **Plateformes concernées :** Cisco Crosswork (Data Gateway, Network Controller, Planning) et Secure Workload (SaaS et sur site).
*   **Nombre de failles :** 9 vulnérabilités au total, dont 5 présentent un score CVSS critique de 10.0.
*   **Origine :** Découvertes lors de tests de sécurité internes.

#### Vulnérabilités identifiées

**Cisco Crosswork (Correctif : version 7.2.1-SP)**
*   **CVE-2026-20030** (10.0) : Injection SQL.
*   **CVE-2026-20357** (10.0) : Absence d'authentification pour une fonction critique.
*   **CVE-2026-20358** (10.0) : Contrôle externe du système de fichiers.
*   **CVE-2026-20359** (9.9) : Protection insuffisante des identifiants.

**Cisco Secure Workload (Correctifs : 3.10.9.1 ou 4.0.4.16)**
*   **CVE-2026-20315** (10.0) : Contrôle d'accès inapproprié (autorisations, authentification).
*   **CVE-2026-20317** (10.0) : Authentification incorrecte (contournement, entrées non fiables).
*   **CVE-2026-20231** (9.9) : Injection de commandes/OS.
*   **CVE-2026-20318** (9.6) : Validation d'entrée inappropriée et traversée de chemin.
*   **CVE-2026-20319** (7.5) : Dépassement de tampon (buffer overflow).

#### Recommandations
*   **Mise à jour immédiate :** Appliquer sans délai les versions correctives mentionnées ci-dessus pour éviter toute exposition.
*   **Veille de sécurité :** Compte tenu de la fréquence des découvertes internes chez Cisco, maintenir une surveillance active des bulletins d'avis de sécurité officiels du constructeur.

---
[Source](https://thehackernews.com/2026/08/cisco-patches-nine-crosswork-and-secure.html){:target="_blank"}
