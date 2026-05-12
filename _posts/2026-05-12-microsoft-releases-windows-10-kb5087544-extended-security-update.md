---
title: 'Microsoft releases Windows 10 KB5087544 extended security update'
date: 2026-05-12
permalink: /posts/2026/05/12/microsoft-releases-windows-10-kb5087544-extended-security-update/
tags:
- veille-cyber
- bleepingcomp
---
### Mise à jour de sécurité Windows 10 KB5087544 (Mai 2026)

Microsoft a publié la mise à jour KB5087544 pour les versions de Windows 10 sous support étendu (ESU) et Enterprise LTSC. Cette mise à jour intègre les correctifs du « Patch Tuesday » de mai 2026, traitant au total 120 vulnérabilités.

**Points clés :**
* **Versions ciblées :** Mise à niveau vers les builds 19045.7291 (Windows 10) et 19044.7291 (LTSC 2021).
* **Sécurité :** Amélioration du reporting d'état pour le *Secure Boot* dans l'application Sécurité Windows et déploiement élargi des certificats *Secure Boot*.
* **Correctifs fonctionnels :** Résolution d'un bug d'affichage des avertissements de sécurité lors de l'utilisation du Bureau à distance (RDP) en multi-écrans et mise à jour des paramètres d'heure d'été pour l'Égypte.

**Vulnérabilités :**
* Bien que 120 vulnérabilités soient corrigées, l'article ne spécifie pas de CVE individuelles. La mise à jour adresse principalement des failles de sécurité critiques liées au Patch Tuesday de mai 2026.

**Problème connu et recommandations :**
* **Problème BitLocker :** Certains systèmes peuvent demander une clé de récupération après l'installation si une configuration de stratégie de groupe spécifique incluant le profil PCR7 est utilisée.
* **Contournement :** Microsoft recommande temporairement de supprimer la stratégie de groupe affectée, puis de suspendre et reprendre le chiffrement BitLocker pour régénérer les liaisons PCR par défaut.
* **Installation :** Les utilisateurs éligibles peuvent installer la mise à jour via **Paramètres > Windows Update > Rechercher des mises à jour**.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-releases-windows-10-kb5087544-extended-security-update/){:target="_blank"}
