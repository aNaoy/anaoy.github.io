---
title: 'ShinyHunters claims FBI hack, data theft in PeopleSoft zero-day breach'
date: 2026-09-23
permalink: /posts/2026/09/23/shinyhunters-claims-fbi-hack-data-theft-in-peoplesoft-zero-day-breach/
tags:
- veille-cyber
- bleepingcomp
---
### Infiltration présumée du FBI par le groupe ShinyHunters via une faille zero-day

Le groupe de cybercriminels ShinyHunters affirme avoir compromis des systèmes du FBI en exploitant une vulnérabilité « zero-day » non corrigée au sein de la plateforme Oracle PeopleSoft. Cette intrusion aurait permis d'exécuter du code à distance et d'accéder à l'infrastructure AWS GovCloud de l'agence, entraînant le vol présumé de 2 à 3 To de données confidentielles concernant des employés, des anciens collaborateurs et des candidats au recrutement. Le FBI a confirmé l'ouverture d'une enquête suite au défaçage du site *fbijobs.gov*.

**Points clés :**
* **Revendication :** Le groupe affirme agir en représailles à un rapport officiel du FBI publié en mai 2026 le concernant.
* **Volume de données :** Le vol porterait sur des informations personnelles identifiables (PII) et des données de santé (PHI). Des échantillons vérifiés partiellement par des tiers semblent confirmer l'authenticité de certaines données.
* **Cibles élargies :** Les attaquants prétendent utiliser la même faille pour cibler d'autres organisations, notamment des entreprises du Fortune 500.
* **Réaction du FBI :** L'agence a immédiatement mis hors ligne les systèmes affectés dès la détection de l'intrusion.

**Vulnérabilités :**
* **Type :** Vulnérabilité zero-day (non corrigée) dans Oracle PeopleSoft permettant l'exécution de code à distance (RCE).
* **CVE :** Aucune CVE n'est actuellement disponible, la vulnérabilité étant présumée inédite et non documentée par l'éditeur.

**Recommandations :**
* **Veille de sécurité :** Les organisations utilisant Oracle PeopleSoft doivent surveiller activement les bulletins de sécurité officiels d'Oracle pour identifier toute mise à jour corrective dès sa publication.
* **Monitoring :** Renforcer la surveillance des logs d'accès, en particulier pour les services exposés, et rechercher des indicateurs de compromission (IoC) liés à une exploitation inhabituelle des fonctionnalités de PeopleSoft.
* **Segmentation :** Appliquer le principe du moindre privilège sur les infrastructures cloud (type AWS GovCloud) pour limiter les mouvements latéraux en cas de compromission initiale d'un service tiers.

---
[Source](https://www.bleepingcomputer.com/news/security/shinyhunters-claims-fbi-hack-data-theft-in-peoplesoft-zero-day-breach/){:target="_blank"}
