---
title: 'Microsoft fixes Classic Outlook bug causing email delivery issues'
date: 2026-04-07
permalink: /posts/2026/04/07/microsoft-fixes-classic-outlook-bug-causing-email-delivery-issues/
tags:
- veille-cyber
- bleepingcomp
---
### Résolution du bug de non-distribution des e-mails dans Classic Outlook

Microsoft a corrigé un dysfonctionnement affectant la version « Classic » d'Outlook, qui empêchait certains utilisateurs d'envoyer des e-mails via Outlook.com. Le problème survenait principalement lorsque le profil Outlook était lié à un compte Exchange ou en cas de conflit avec un contact de messagerie Exchange Online possédant la même adresse SMTP.

**Points clés :**
*   **Symptômes :** Les utilisateurs recevaient des rapports de non-distribution (NDR) contenant les codes d'erreur `0x80070005-0x0004dc-0x000524`.
*   **Correction :** Microsoft a déployé un correctif côté serveur le 3 avril 2026.
*   **Vulnérabilités :** Aucune CVE n'a été attribuée à cet incident, car il s'agit d'un bug de fonctionnalité technique et non d'une faille de sécurité exploitable.

**Recommandations :**
*   **Mise à jour :** Le correctif étant appliqué côté serveur, aucune action manuelle de mise à jour du logiciel n'est requise.
*   **Contournements temporaires :** En cas de persistance, il est conseillé d'utiliser le « New Outlook » ou la version web d'Outlook.com. Alternativement, le téléchargement manuel du carnet d'adresses Outlook pour les comptes concernés peut résoudre le problème.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-classic-outlook-bug-causing-email-delivery-issues/){:target="_blank"}
