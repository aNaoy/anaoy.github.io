---
title: 'Microsoft says Copilot buttons still missing in classic Outlook'
date: 2026-09-16
permalink: /posts/2026/09/16/microsoft-says-copilot-buttons-still-missing-in-classic-outlook/
tags:
- veille-cyber
- bleepingcomp
---
### Dysfonctionnement des boutons Copilot dans Outlook Classique

Microsoft enquête sur un bug persistant affectant les utilisateurs d'Outlook Classique (build 20026.20182 et supérieures), où les boutons Copilot disparaissent de l'interface. Le problème est lié à une incapacité d'Outlook à localiser la propriété MAPI `PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W` dans le profil utilisateur, empêchant la persistance des paramètres liés à Copilot.

**Points clés :**
*   **Impact :** Les utilisateurs disposant d'une licence Copilot Chat ou M365 Copilot ne voient plus les accès rapides à Copilot (ruban, barre latérale).
*   **Comportement :** L'outil peut apparaître comme disponible dans les options, mais reste non fonctionnel ou grisé.
*   **Incidents connexes :** Un bug distinct provoque des plantages d'Outlook (Événement 1000) sur les systèmes utilisant l'antivirus Kaspersky via le module `mcou.dll`.

**Vulnérabilités :**
*   Aucune CVE associée à ce jour ; il s'agit d'un dysfonctionnement logiciel interne (bug applicatif).

**Recommandations :**
*   **Contournement temporaire :** Activer l'option « Afficher les applications dans Outlook » via *Fichier > Options > Avancé > Volets Outlook*.
*   **Alternatives :** Utiliser Outlook sur le web (OWA), la nouvelle version d'Outlook ou créer un nouveau profil Outlook.
*   **Pour les plantages Kaspersky :** Contacter directement le support technique de Kaspersky.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-shares-workaround-for-missing-outlook-copilot-buttons/){:target="_blank"}
