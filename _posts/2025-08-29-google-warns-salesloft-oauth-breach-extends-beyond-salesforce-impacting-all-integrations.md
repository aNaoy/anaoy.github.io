---
title: 'Google Warns Salesloft OAuth Breach Extends Beyond Salesforce, Impacting All Integrations'
date: 2025-08-29
permalink: /posts/2025/08/29/google-warns-salesloft-oauth-breach-extends-beyond-salesforce-impacting-all-integrations/
tags:
- veille-cyber
- hackernews
---
### Compromission d'OAuth Salesloft : Impact Étendu sur les Intégrations

Une campagne de vol de données opportuniste exploite des jetons OAuth compromis liés à Salesloft Drift pour cibler des instances Salesforce. Initialement centrée sur Salesforce, l'attaque s'avère plus vaste et affecte toutes les intégrations utilisant la plateforme Drift.

Des acteurs malveillants, identifiés comme UNC6395, ont utilisé ces jetons volés pour accéder à des courriels provenant d'un petit nombre de comptes Google Workspace, spécifiquement ceux configurés pour s'intégrer à Salesloft. Google a notifié les utilisateurs concernés, révoqué les jetons OAuth affectés et désactivé l'intégration entre Google Workspace et Salesloft Drift.

Salesforce a également pris des mesures en désactivant temporairement toutes les intégrations avec Salesloft, bien que Salesloft déclare qu'aucune activité malveillante n'a été détectée dans ses propres intégrations suite à l'incident Drift.

**Points Clés :**

*   Une campagne de vol de données utilise des jetons OAuth compromis de Salesloft Drift.
*   L'impact s'étend au-delà de Salesforce à toutes les intégrations de Drift.
*   Des comptes Google Workspace ont été potentiellement accédés via l'intégration "Drift Email".
*   Salesforce a désactivé temporairement toutes les intégrations avec Salesloft.

**Vulnérabilités :**

*   La compromission des jetons OAuth liés à l'intégration "Drift Email" de Salesloft.
*   Aucun identifiant CVE spécifique n'est mentionné dans l'article pour cette vulnérabilité.

**Recommandations :**

*   Traiter tous les jetons d'authentification stockés ou connectés à la plateforme Drift comme potentiellement compromis.
*   Examiner toutes les intégrations tierces connectées à votre instance Drift.
*   Révoquer et faire pivoter les identifiants pour ces applications connectées.
*   Enquêter sur tous les systèmes connectés pour détecter tout signe d'accès non autorisé.

---
[Source](https://thehackernews.com/2025/08/google-warns-salesloft-oauth-breach.html){:target="_blank"}
