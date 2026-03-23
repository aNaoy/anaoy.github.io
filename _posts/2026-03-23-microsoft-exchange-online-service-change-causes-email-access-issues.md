---
title: 'Microsoft Exchange Online service change causes email access issues'
date: 2026-03-23
permalink: /posts/2026/03/23/microsoft-exchange-online-service-change-causes-email-access-issues/
tags:
- veille-cyber
- bleepingcomp
---
### Perturbation de l'accès à Exchange Online

Microsoft subit actuellement une interruption intermittente des services Exchange Online, empêchant certains utilisateurs d'accéder à leurs boîtes mail via l'application Outlook mobile et le nouveau client Outlook pour Mac.

**Points clés :**
*   **Cause identifiée :** L'incident (référencé sous le code **EX1256020**) a été provoqué par l'introduction d'un nouveau compte virtuel au sein de l'infrastructure.
*   **Action en cours :** Microsoft a entamé la désactivation de ce changement pour rétablir un accès normal, après l'échec d'une tentative de redémarrage des serveurs.
*   **Contexte :** Il s'agit de la quatrième panne majeure d'Exchange Online signalée depuis novembre, témoignant d'une instabilité récurrente des services cloud de Microsoft.

**Vulnérabilités :**
*   Aucune vulnérabilité de type CVE n'est associée à cet incident. Il s'agit d'une erreur opérationnelle liée à une mise à jour logicielle ("service change") plutôt qu'à une faille de sécurité exploitable.

**Recommandations :**
*   **Administrateurs :** Surveiller le centre d'administration Microsoft 365 (Message Center) pour obtenir les mises à jour en temps réel sur l'incident EX1256020.
*   **Continuité :** En cas d'impossibilité d'accéder aux mails, privilégier temporairement l'utilisation d'Outlook sur le Web (OWA) ou d'autres protocoles de connexion non affectés par cette mise à jour spécifique si les accès clients (mobile/Mac) restent bloqués.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/new-exchange-online-virtual-account-blocks-email-access-via-mobile-mac-apps/){:target="_blank"}
