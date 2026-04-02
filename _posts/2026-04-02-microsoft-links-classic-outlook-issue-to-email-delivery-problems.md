---
title: 'Microsoft links Classic Outlook issue to email delivery problems'
date: 2026-04-02
permalink: /posts/2026/04/02/microsoft-links-classic-outlook-issue-to-email-delivery-problems/
tags:
- veille-cyber
- bleepingcomp
---
### Problèmes d'envoi d'e-mails sous Classic Outlook

Microsoft enquête sur un bug affectant « Classic Outlook » qui empêche certains utilisateurs d'envoyer des e-mails via Outlook.com. Ce dysfonctionnement survient principalement lorsque le compte Outlook.com utilisé est lié à un autre compte Exchange, ou lorsqu'il existe un conflit avec un contact mail Exchange Online possédant la même adresse SMTP.

**Points clés :**
*   **Symptômes :** Les utilisateurs reçoivent un rapport de non-distribution (NDR) avec l'erreur `[0x80070005-0x0004dc-0x000524]` indiquant une absence de permission pour envoyer des messages au nom de l'utilisateur spécifié.
*   **Vulnérabilités :** Aucun identifiant CVE n'est associé à ce problème ; il s'agit d'un bug fonctionnel de synchronisation et de gestion des permissions au sein de l'architecture Outlook.

**Recommandations :**
*   **Retrait du carnet d'adresses :** Supprimer le carnet d'adresses M365 afin d'éviter la vérification lors de l'envoi.
*   **Masquage des contacts :** Cacher le contact Outlook.com de la liste d'adresses globale (GAL) du compte Microsoft 365.
*   **Profil dédié :** Créer un nouveau profil « Classic Outlook » contenant uniquement le compte impacté.
*   **Solutions alternatives :** Utiliser la version « New Outlook » (client moderne) ou accéder directement à Outlook.com via un navigateur web.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-links-classic-outlook-bug-to-email-delivery-issues/){:target="_blank"}
