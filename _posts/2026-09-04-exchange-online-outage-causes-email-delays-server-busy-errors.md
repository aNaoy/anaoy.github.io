---
title: 'Exchange Online outage causes email delays, Server busy errors'
date: 2026-09-04
permalink: /posts/2026/09/04/exchange-online-outage-causes-email-delays-server-busy-errors/
tags:
- veille-cyber
- bleepingcomp
---
### Perturbations majeures sur Exchange Online

Microsoft a rencontré une interruption de service sur Exchange Online (incident suivi sous la référence **EX1467029**), provoquant des retards significatifs et des erreurs « Server busy » lors de l'envoi ou de la réception d'e-mails vers des domaines externes. L'enquête initiale a révélé que les mécanismes de protection anti-spam ont aggravé les délais de traitement pour une partie des utilisateurs. La situation est désormais stabilisée, Microsoft procédant à la surveillance des files d'attente pour confirmer le retour à la normale.

**Points clés :**
*   **Nature de l'incident :** Dysfonctionnement affectant le flux de courrier électronique externe.
*   **Impact :** Erreurs intermittentes « Server busy » et retards de livraison.
*   **Cause identifiée :** Problèmes de traitement exacerbés par les protections anti-spam.
*   **Statut :** Résolu pour les nouveaux e-mails ; surveillance en cours.

**Vulnérabilités :**
*   Aucune vulnérabilité logicielle (CVE) n'est associée à cet incident de service ; il s'agit d'une défaillance opérationnelle liée à l'infrastructure cloud.

**Recommandations :**
*   **Patience pour les envois différés :** La plupart des clients de messagerie tentent automatiquement de renvoyer les e-mails bloqués.
*   **Vérification des NDR (Non-Delivery Reports) :** Si un rapport de non-remise est reçu après 24 à 72 heures, l'expéditeur doit manuellement renvoyer le message concerné.
*   **Suivi de l'état des services :** Consulter régulièrement le centre d'administration Microsoft 365 (Service Health) lors de pannes similaires pour obtenir des mises à jour en temps réel.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/exchange-online-outage-causes-email-delays-server-busy-errors/){:target="_blank"}
