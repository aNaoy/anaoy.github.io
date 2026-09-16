---
title: 'Microsoft says Copilot buttons still missing in classic Outlook'
date: 2026-09-16
permalink: /posts/2026/09/16/microsoft-says-copilot-buttons-still-missing-in-classic-outlook/
tags:
- veille-cyber
- bleepingcomp
---
### Dysfonctionnement de Microsoft Copilot dans l'Outlook classique

Microsoft enquête sur un bug persistant provoquant la disparition des boutons Copilot dans la version "classique" d'Outlook pour Windows (build 20026.20182 et supérieures). Ce dysfonctionnement empêche l'accès aux fonctionnalités d'IA, bien que le service reste opérationnel via le web ou l'application autonome.

**Points clés :**
* **Cause identifiée :** Outlook ne parvient pas à localiser la propriété MAPI `PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W`, empêchant le chargement correct des paramètres Copilot.
* **Impact :** Disparition des boutons Copilot, icônes inactives ou commandes grisées dans le ruban.
* **Problème connexe :** Des plantages d'Outlook ont été signalés sur les systèmes utilisant l'antivirus Kaspersky, liés au module `mcou.dll`.

**Vulnérabilités :**
Aucune CVE n'est associée à ces dysfonctionnements. Il s'agit de problèmes de compatibilité logicielle et de configuration de profil.

**Recommandations :**
* **Contournement temporaire :** Dans Outlook, accédez à *Fichier > Options > Avancé* et cochez l'option "Afficher les applications dans Outlook" (Show Apps in Outlook).
* **Alternatives :** Utiliser Outlook sur le web (OWA), la nouvelle version d'Outlook, ou créer un nouveau profil Outlook.
* **Pour les plantages liés à Kaspersky :** Contacter directement le support technique de Kaspersky.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-shares-workaround-for-missing-outlook-copilot-buttons/){:target="_blank"}
