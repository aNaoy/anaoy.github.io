---
title: 'FBI Removes Accenture Contractor After Patch Failure Led to ShinyHunters Breach'
date: 2026-10-06
permalink: /posts/2026/10/06/fbi-removes-accenture-contractor-after-patch-failure-led-to-shinyhunters-breach/
tags:
- veille-cyber
- hackernews
---
### Faille de sécurité chez le FBI : le rôle critique de la gestion des correctifs

Le FBI a rompu son contrat avec un prestataire d'Accenture suite à une intrusion du groupe de cybercriminels « ShinyHunters ». Cet incident a permis le vol des données personnelles de milliers d'employés du Bureau via son portail emploi. L'enquête a révélé que la brèche est directement imputable à la négligence d'un prestataire n'ayant pas appliqué un correctif de sécurité critique sur une plateforme Oracle PeopleSoft gérée par des tiers.

**Points clés :**
*   **Origine de l'attaque :** Exploitation du portail emploi du FBI via une plateforme Oracle PeopleSoft mal sécurisée.
*   **Conséquences :** Exfiltration des données personnelles de milliers d'employés et éviction du prestataire responsable.
*   **Contexte :** Le groupe ShinyHunters est au cœur de l'enquête ; deux membres ont déjà été arrêtés, et d'autres interpellations sont attendues.

**Vulnérabilité identifiée :**
*   **CVE-2026-35273 :** Les attaquants contournent les règles des pare-feu applicatifs (WAF) protégeant le point de terminaison *Environment Management Hub* (PSEMHUB) en utilisant une technique de double encodage d'URL pour masquer l'exploitation.

**Recommandations :**
*   **Gestion rigoureuse des correctifs :** Appliquer systématiquement et sans délai les mises à jour de sécurité critiques sur tous les actifs tiers exposés.
*   **Audit des accès tiers :** Renforcer le contrôle et la supervision des prestataires externes ayant des droits de gestion sur les infrastructures critiques.
*   **Renforcement des WAF :** Mettre à jour les signatures et les règles de filtrage pour contrer les techniques d'obfuscation (comme l'encodage d'URL) ciblant les vulnérabilités connues.

---
[Source](https://thehackernews.com/2026/10/fbi-removes-accenture-contractor-after.html){:target="_blank"}
