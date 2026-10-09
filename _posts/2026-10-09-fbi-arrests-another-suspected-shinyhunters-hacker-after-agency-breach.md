---
title: 'FBI arrests another suspected ShinyHunters hacker after agency breach'
date: 2026-10-09
permalink: /posts/2026/10/09/fbi-arrests-another-suspected-shinyhunters-hacker-after-agency-breach/
tags:
- veille-cyber
- bleepingcomp
---
### Intensification des arrestations contre le groupe de hackers ShinyHunters

Le FBI a procédé à l'arrestation d'un nouveau suspect, un citoyen canadien interpellé en Pennsylvanie, considéré comme un co-conspirateur clé du groupe d'extorsion ShinyHunters. Cette opération fait suite à l'intrusion récente dans la plateforme *FBIJobs.gov*, gérée par un prestataire tiers.

**Points clés :**
* **Infiltration :** Le groupe a accédé aux systèmes du FBI en exploitant une vulnérabilité « zero-day » dans Oracle PeopleSoft, avant de se déplacer latéralement vers l'infrastructure AWS GovCloud du Bureau.
* **Volume de données :** Environ 2 à 3 To de données ont été dérobés, contenant des informations sensibles sur les employés, les candidats et des dossiers médicaux/psychiatriques.
* **Stratégie du FBI :** Les autorités multiplient les pressions et les arrestations internationales (Pays-Bas, Jordanie, États-Unis) pour démanteler le réseau, incitant les membres restants à se rendre.
* **Modus Operandi :** ShinyHunters est spécialisé dans le vol de données via des applications web/SaaS, le hameçonnage vocal (vishing) ciblant les comptes SSO (Okta, Microsoft, Google) et l'extorsion de données.

**Vulnérabilités :**
* **Oracle PeopleSoft :** Exploitation d'une vulnérabilité « zero-day » (non spécifiée par un identifiant CVE public dans l'article).
* **Gestion des correctifs :** Le défaut d'installation d'une mise à jour de sécurité sur une plateforme tierce a permis l'intrusion.

**Recommandations :**
* **Mise à jour des systèmes :** Appliquer immédiatement les correctifs de sécurité sur toutes les infrastructures, y compris celles gérées par des prestataires tiers.
* **Sécurisation des accès :** Renforcer la protection des comptes SSO contre le vishing et le vol de jetons d'authentification (MFA).
* **Gestion des prestataires :** Auditer rigoureusement les tiers ayant accès aux environnements cloud et aux données sensibles de l'organisation.

---
[Source](https://www.bleepingcomputer.com/news/security/fbi-arrests-another-suspected-shinyhunters-hacker-after-agency-breach/){:target="_blank"}
