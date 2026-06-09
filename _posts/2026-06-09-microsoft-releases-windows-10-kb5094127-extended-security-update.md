---
title: 'Microsoft releases Windows 10 KB5094127 extended security update'
date: 2026-06-09
permalink: /posts/2026/06/09/microsoft-releases-windows-10-kb5094127-extended-security-update/
tags:
- veille-cyber
- bleepingcomp
---
### Mise à jour de sécurité étendue Windows 10 KB5094127

Microsoft a publié la mise à jour KB5094127 pour les systèmes Windows 10 Enterprise LTSC et les utilisateurs du programme ESU (Extended Security Update). Cette mise à jour corrige les vulnérabilités identifiées lors du Patch Tuesday de juin 2026 et introduit des mécanismes de gestion pour les nouveaux certificats Secure Boot.

**Points clés :**
*   **Version système :** La mise à jour fait passer Windows 10 à la version 19045.7417 (ou 19044.7417 pour l'édition LTSC 2021).
*   **Secure Boot :** Introduction de rapports d'état dynamiques dans l'application Sécurité Windows et ajout d'une règle de stratégie de groupe (`LimitSecureBootRequiredServiceData`) permettant de limiter l'envoi de données de télémétrie à Microsoft.
*   **Amélioration fonctionnelle :** Optimisation de la recherche dans l'Explorateur de fichiers (support du chinois et des fichiers encodés en UTF-8 sans BOM).

**Vulnérabilités :**
*   Le correctif inclut la résolution de **200 vulnérabilités** traitées lors du Patch Tuesday de juin 2026, dont **3 failles "zero-day"** divulguées publiquement (les identifiants CVE spécifiques ne sont pas listés dans l'article source).

**Recommandations :**
*   **Installation :** Procéder à l'installation via Windows Update pour les systèmes éligibles (Enterprise LTSC ou programme ESU).
*   **BitLocker :** La mise à jour peut déclencher des invites de récupération BitLocker sur certains systèmes (configuration spécifique PCR7/TPM). En cas de blocage, Microsoft préconise de retirer la stratégie de groupe concernée, puis de suspendre et réactiver BitLocker pour régénérer les liaisons PCR par défaut.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-releases-windows-10-kb5094127-extended-security-update/){:target="_blank"}
