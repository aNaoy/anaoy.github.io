---
title: 'Abbott probes two cyber incidents amid extortion claims'
date: 2026-07-18
permalink: /posts/2026/07/18/abbott-probes-two-cyber-incidents-amid-extortion-claims/
tags:
- veille-cyber
- bleepingcomp
---
### Incidents de cybersécurité chez Abbott Laboratories : Double intrusion présumée

Abbott Laboratories fait face à deux incidents de cybersécurité distincts : l'un concernant ses systèmes hérités « Exact Sciences » et l'autre ciblant son portail client « LabCentral ».

**Points clés :**
*   **Incident Exact Sciences :** Le groupe d'extorsion **ShinyHunters** revendique une intrusion après une attaque par *vishing* (phishing vocal) visant des employés, permettant la compromission d'un compte Microsoft Entra (SSO). Le groupe prétend avoir exfiltré 30 millions d'entrées d'informations personnelles (PII) et des millions de documents médicaux confidentiels.
*   **Incident LabCentral :** Le groupe **ShadowByt3$** affirme avoir compromis le portail client LabCentral via des identifiants clients dérobés pour accéder à des données techniques. Abbott conteste la nature sensible des données, affirmant qu'il ne s'agit que de documents techniques publics.
*   **Impact opérationnel :** Abbott précise que ces incidents n'affectent ni ses opérations commerciales, ni ses capacités de production, ni la prise en charge des patients.

**Vulnérabilités :**
*   **Ingénierie sociale :** Utilisation du *vishing* pour contourner les contrôles d'authentification.
*   **Compromission de SSO :** Exploitation de comptes Microsoft Entra pour s'introduire latéralement dans des applications SaaS (Salesforce, SharePoint, etc.).
*   **Authentification faible :** Usage d'identifiants clients compromis sur le portail LabCentral.
*   *Note : Aucune CVE spécifique n'est associée à ces incidents, qui reposent sur des vecteurs d'attaque humains et de gestion des identités.*

**Recommandations :**
*   **Renforcement de l'authentification :** Généraliser l'authentification multifacteur (MFA) résistante au phishing (ex: jetons FIDO2/WebAuthn) pour tous les comptes SSO.
*   **Formation des employés :** Sensibiliser spécifiquement le personnel aux tactiques de *vishing* et d'ingénierie sociale.
*   **Surveillance des accès :** Mettre en place une surveillance accrue des API et des activités suspectes sur les portails clients et les environnements SaaS.
*   **Gestion des identités :** Appliquer le principe du moindre privilège aux comptes SSO connectés aux applications critiques pour limiter l'exfiltration de données en cas de compromission.

---
[Source](https://www.bleepingcomputer.com/news/security/abbott-laboratories-probes-two-cyber-incidents-amid-extortion-claims/){:target="_blank"}
