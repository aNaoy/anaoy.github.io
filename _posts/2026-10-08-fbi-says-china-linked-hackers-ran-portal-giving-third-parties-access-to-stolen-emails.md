---
title: 'FBI Says China-Linked Hackers Ran Portal Giving Third Parties Access to Stolen Emails'
date: 2026-10-08
permalink: /posts/2026/10/08/fbi-says-china-linked-hackers-ran-portal-giving-third-parties-access-to-stolen-emails/
tags:
- veille-cyber
- hackernews
---
### Espionnage et vol de données par Integrity Technology Group

Des agences internationales, menées par le FBI, ont mis en lumière les activités d'**Integrity Technology Group**, une entreprise chinoise impliquée dans une campagne d'espionnage informatique de longue haleine. Utilisant des outils d'automatisation et de l'intelligence artificielle, ce groupe cible des gouvernements, des institutions médicales, religieuses et des services de maintien de l'ordre à travers le monde pour exfiltrer des courriels et des données sensibles, qu'il rend parfois accessibles à des tiers via un portail web dédié.

#### Points clés
*   **Mode opératoire :** Utilisation de scanners automatisés (comme *MicroScan*) pour détecter des vulnérabilités, attaques par "password spraying" (via l'outil *EBurst*) et exfiltration de courriels via des scripts PHP.
*   **Persistance :** Installation de VPN légitimes (SoftEther) renommés pour passer inaperçus et utilisation de la technique DCSync pour voler des identifiants Active Directory.
*   **Infrastructure :** Le groupe a été lié au botnet *Raptor Train* (neutralisé en 2024), comprenant plus de 200 000 appareils compromis.
*   **Portée :** Activités documentées depuis au moins 2021, avec des cibles en Asie du Sud-Est, Afrique et Amérique du Nord.

#### Vulnérabilités exploitées (CVE)
Le groupe exploite activement huit failles majeures dans des logiciels tiers :
*   **CVE-2014-6278** (GNU Bash)
*   **CVE-2015-3306** (ProFTPD)
*   **CVE-2015-5477** (ISC BIND)
*   **CVE-2016-3081** (Apache Struts)
*   **CVE-2019-11510** (Pulse Connect Secure)
*   **CVE-2021-22205** (GitLab)
*   **CVE-2021-3199** (ONLYOFFICE Document Server)
*   **CVE-2023-22894** (Strapi)

#### Recommandations de sécurité
*   **Mises à jour :** Appliquer immédiatement les correctifs pour les vulnérabilités listées ci-dessus.
*   **Authentification :** Imposer l'authentification multifacteur (MFA) pour tous les accès distants, webmails et systèmes critiques.
*   **Durcissement réseau :** Désactiver les services, ports et protocoles de gestion à distance inutilisés.
*   **Surveillance :** Inspecter les journaux à la recherche d'activités suspectes liées à la réplication Active Directory (DCSync) et auditer les applications tierces connectées aux services cloud (Microsoft 365).
*   **Hygiène web :** Assainir les entrées utilisateur pour prévenir les attaques de type XSS (Cross-Site Scripting).

---
[Source](https://thehackernews.com/2026/10/fbi-says-china-linked-hackers-ran.html){:target="_blank"}
