---
title: 'New InfraTrust report reveals infrastructure flaws admins should patch first'
date: 2026-07-22
permalink: /posts/2026/07/22/new-infratrust-report-reveals-infrastructure-flaws-admins-should-patch-first/
tags:
- veille-cyber
- bleepingcomp
---
### Priorisation de la sécurité des infrastructures : Rapport InfraTrust

Eclypsium a lancé **InfraTrust**, une base de connaissances et un rapport mensuel visant à aider les administrateurs à prioriser les correctifs de sécurité. Contrairement aux scores CVSS classiques, cette approche privilégie l'exploitabilité réelle, l'exposition sur internet et le risque opérationnel, notamment face aux menaces étatiques ciblant les équipements réseau et périphériques.

#### Points clés
*   **Vulnérabilités critiques :** Le premier rapport identifie 61 avis, dont 6 critiques et 26 exploitables à distance sans authentification.
*   **Focus sur le périmètre :** Les équipements exposés (pare-feux, VPN, routeurs) constituent la cible principale des groupes de pirates soutenus par des États (type Volt Typhoon).
*   **Risque lié au firmware :** Les mises à jour matérielles dépendent souvent des constructeurs, créant un décalage dangereux entre la découverte d'une faille et sa correction effective.

#### Vulnérabilités prioritaires à corriger
| Équipement | CVE associés / Référence | Risque principal |
| :--- | :--- | :--- |
| **SonicWall SMA1000** | CVE-2026-15409, CVE-2026-15410 | Exploitation active (RCE) |
| **Fortinet FortiSandbox** | CVE-2026-39808, CVE-2026-25089 | Injection de commande (KEV CISA) |
| **Dell EMC Networking OS10** | DSA-2026-240 | Faille Linux exploitée activement |
| **F5 BIG-IP** | K000161837 | Faille mémoire sans authentification |
| **Juniper Junos OS** | JSA110083, JSA110086 | Déni de service (DoS) à distance |

#### Recommandations stratégiques
1.  **Changer de modèle de priorisation :** Ne pas se fier uniquement au score CVSS. Prioriser les failles présentes sur des actifs exposés sur internet et celles listées dans le catalogue **CISA KEV** (Known Exploited Vulnerabilities).
2.  **Surveiller les équipements réseau :** Accorder une attention particulière aux passerelles d'accès distant et aux contrôleurs de livraison d'applications, souvent vecteurs d'entrée privilégiés.
3.  **Anticiper le délai des constructeurs :** Dans le cas des composants matériels (SmartNIC, BIOS, DPU), vérifier régulièrement les bulletins spécifiques des OEM, car les correctifs de sécurité amont (ex: Linux, Qualcomm) mettent souvent du temps à être intégrés dans les firmwares propriétaires.

---
[Source](https://www.bleepingcomputer.com/news/security/new-infratrust-report-reveals-infrastructure-flaws-admins-should-patch-first/){:target="_blank"}
