---
title: 'Microsoft still working to fix Exchange Online mailbox access issues'
date: 2026-04-03
permalink: /posts/2026/04/03/microsoft-still-working-to-fix-exchange-online-mailbox-access-issues/
tags:
- veille-cyber
- bleepingcomp
---
### Instabilité persistante de l'accès à Exchange Online

Microsoft peine à résoudre des problèmes d'accès intermittents aux boîtes mail Exchange Online, affectant principalement les utilisateurs d'Outlook sur mobile et sur macOS. Malgré une première tentative de correction début avril, l'incident a été réactivé (ID de suivi : EX1268771).

**Points clés :**
*   **Origine :** Le problème a débuté le 11 mars, initialement attribué à un nouveau "compte virtuel".
*   **Impact :** Interruption sporadique de la connexion pour les utilisateurs mobiles et les clients Outlook pour Mac.
*   **Actions en cours :** Les équipes techniques travaillent sur le redémarrage du service « Notification Broker » pour stabiliser l'accès tout en poursuivant l'analyse de la cause profonde.
*   **Historique :** Cet incident s'inscrit dans une série de pannes récentes touchant divers protocoles de connexion (IMAP4, Exchange ActiveSync) et services Microsoft 365.

**Vulnérabilités :**
*   Aucune vulnérabilité de sécurité (CVE) n'est associée à cet incident ; il s'agit d'une défaillance technique opérationnelle et non d'une faille exploitable.

**Recommandations :**
*   **Surveillance :** Les administrateurs système doivent consulter régulièrement le centre de messages Microsoft 365 (via les IDs EX1256020 et EX1268771) pour obtenir les mises à jour en temps réel sur la résolution.
*   **Contournement temporaire :** En cas de blocage persistant, les utilisateurs peuvent tenter d'accéder à leurs mails via la version web d'Outlook, qui ne semble pas être impactée par ce bug spécifique.
*   **Support :** Ouvrir un ticket de support auprès de Microsoft si l'accès reste totalement bloqué pour des comptes critiques au sein de l'organisation.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-still-working-to-fix-exchange-online-mailbox-access-issues/){:target="_blank"}
