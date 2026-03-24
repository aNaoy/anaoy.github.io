---
title: 'Crunchyroll probes breach after hacker claims to steal 6.8M users data'
date: 2026-03-24
permalink: /posts/2026/03/24/crunchyroll-probes-breach-after-hacker-claims-to-steal-68m-users-data/
tags:
- veille-cyber
- bleepingcomp
---
### Violation de données chez Crunchyroll : L'impact des prestataires tiers

Crunchyroll fait l'objet d'une enquête suite à une compromission ayant permis l'exfiltration de données appartenant à environ 6,8 millions d'utilisateurs. L'incident découle de l'infection par un logiciel malveillant de l'ordinateur d'un agent de support technique travaillant pour **Telus International**, un prestataire de services externalisés (BPO).

**Points clés :**
*   **Vecteur d'attaque :** Utilisation d'un malware pour dérober les identifiants Okta (SSO) d'un employé du prestataire.
*   **Accès obtenus :** Les attaquants ont accédé à des outils critiques, notamment Zendesk, Slack, Google Workspace et Jiro Service Management.
*   **Volume de données :** Environ 8 millions de tickets de support téléchargés, contenant 6,8 millions d'adresses e-mail uniques.
*   **Données exposées :** Noms, noms d'utilisateur, adresses IP, localisations et contenus des tickets de support. Certaines informations de cartes bancaires (partielles) ont été dérobées lorsqu'elles avaient été saisies par les clients dans les tickets.
*   **Extorsion :** Les pirates ont tenté de rançonner Crunchyroll à hauteur de 5 millions de dollars, sans succès.

**Vulnérabilités :**
*   **Compromission d'identifiants SSO :** Accès non autorisé via des comptes privilégiés de prestataires tiers.
*   **Vulnérabilité de la chaîne d'approvisionnement (Supply Chain) :** Dépendance sécuritaire vis-à-vis des accès accordés aux employés des BPO.
*   *Note : Aucune CVE spécifique n'est associée à cet incident, celui-ci relevant d'une compromission de compte et d'une attaque par malware ciblant le point de terminaison.*

**Recommandations :**
*   **Renforcer l'authentification :** Imposer des méthodes d'authentification multi-facteurs (MFA) robustes et résistantes au phishing pour tous les accès distants et SaaS.
*   **Principe du moindre privilège :** Restreindre strictement les accès des employés de prestataires tiers aux seules données et outils nécessaires à leurs fonctions.
*   **Surveillance des terminaux :** Déployer des solutions EDR (Endpoint Detection and Response) avancées sur les postes des prestataires pour détecter les infections par malwares en temps réel.
*   **Gestion des risques tiers :** Auditer régulièrement les pratiques de sécurité des partenaires BPO et exiger des normes de protection équivalentes aux politiques internes.

---
[Source](https://www.bleepingcomputer.com/news/security/crunchyroll-probes-breach-after-hacker-claims-to-steal-68m-users-data/){:target="_blank"}
