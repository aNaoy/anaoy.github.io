---
title: 'Microsoft releases Windows 10 KB5126657 extended security update'
date: 2026-10-14
permalink: /posts/2026/10/14/microsoft-releases-windows-10-kb5126657-extended-security-update/
tags:
- veille-cyber
- bleepingcomp
---
### Mise à jour de sécurité Windows 10 KB5126657

Microsoft a déployé la mise à jour de sécurité étendue KB5126657 pour Windows 10 (versions Enterprise LTSC et systèmes inscrits au programme ESU). Cette mise à jour intègre les correctifs du Patch Tuesday d'octobre 2026, incluant la résolution de 1 411 vulnérabilités, dont une faille « zero-day » actuellement exploitée.

**Points clés :**
* **Corrections système :** Résolution d'un problème empêchant les disques virtuels *Storage Spaces Direct* de se monter après une mise à jour et correction d'un dysfonctionnement de l'historique des fichiers vers des supports externes.
* **Sécurité ReFS :** Ajout d'audits et de contrôles de politique optionnels pour les volumes ReFS sur les périphériques de stockage externes.
* **Fuseaux horaires :** Mise à jour du support des heures d'été pour le Canada et introduction du fuseau horaire "Manitoba Standard Time".
* **Secure Boot :** Poursuite du déploiement des certificats de démarrage sécurisé mis à jour.

**Vulnérabilités :**
* L'article mentionne le traitement de 1 411 vulnérabilités, incluant une faille « zero-day » active, sans toutefois lister les identifiants CVE spécifiques dans le texte fourni.

**Recommandations :**
* **Installation :** Les utilisateurs éligibles (Enterprise LTSC ou souscripteurs ESU) doivent installer la mise à jour via Windows Update.
* **Gestion des périphériques :** Les administrateurs doivent évaluer les nouveaux contrôles de sécurité pour les volumes ReFS (détails dans la documentation [KB5130741](https://support.microsoft.com/en-us/help/5130741)).
* **Problèmes connus :** Attention à un bug persistant affectant certains périphériques audio USB (Classe 1.0) pouvant entraîner des erreurs de type « Code 10 » ou des dysfonctionnements du son. Microsoft travaille actuellement sur des correctifs supplémentaires pour résoudre les problèmes audio restants.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-releases-windows-10-kb5126657-extended-security-update/){:target="_blank"}
