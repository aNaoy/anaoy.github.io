---
title: 'Microsoft Discloses Exchange Server Flaw Enabling Silent Cloud Access in Hybrid Setups'
date: 2025-08-07
permalink: /posts/2025/08/07/microsoft-discloses-exchange-server-flaw-enabling-silent-cloud-access-in-hybrid-setups/
tags:
- veille-cyber
- hackernews
---
### Accès Cloud Silencieux sur Exchange Server Hybride

Une faille de sécurité critique (CVE-2025-53786, score CVSS de 8.0) a été identifiée dans les versions sur site d'Exchange Server. Elle permet à un attaquant disposant déjà d'un accès administratif à un serveur Exchange sur site d'obtenir des privilèges élevés dans l'environnement cloud connecté, sans laisser de traces facilement détectables. Cette vulnérabilité découle du partage du même principal de service entre Exchange Server et Exchange Online dans les configurations hybrides. L'exploitation peut mener à l'usurpation d'identité d'utilisateurs hybrides pendant 24 heures si la propriété "trustedfordelegation" est activée, sans générer de logs lors de l'émission des jetons. Microsoft prévoit de rendre obligatoire la séparation des principaux de service Exchange sur site et Exchange Online d'ici octobre 2025. Des mesures temporaires incluent le blocage du trafic des Services Web Exchange (EWS) utilisant le principal de service partagé d'Exchange Online.

**Points Clés :**

*   **Vulnérabilité :** CVE-2025-53786
*   **Impact :** Escalade de privilèges silencieuse dans l'environnement cloud d'une organisation hybride, potentiellement jusqu'à l'usurpation d'identité d'utilisateurs.
*   **Condition préalable :** Accès administratif à un serveur Exchange sur site.
*   **Cause :** Partage du même principal de service entre Exchange Server sur site et Exchange Online dans les configurations hybrides.
*   **Découverte :** Signalée par Dirk-jan Mollema (Outsider Security).
*   **Contexte supplémentaire :** L'article mentionne également des artefacts malveillants associés à des vulnérabilités SharePoint récemment divulguées (ToolShell).

**Vulnérabilités :**

*   **CVE-2025-53786 :** Permet l'escalade de privilèges silencieuse dans les environnements Exchange hybrides.

**Recommandations :**

*   Examiner les changements de sécurité pour les déploiements hybrides d'Exchange Server.
*   Installer la mise à jour corrective d'avril 2025 (ou une version plus récente).
*   Suivre les instructions de configuration pour les déploiements hybrides.
*   Réinitialiser les "keyCredentials" du principal de service pour les configurations hybrides antérieures ou les authentifications OAuth qui ne sont plus utilisées.
*   Déconnecter d'Internet les versions obsolètes (fin de vie ou fin de service) d'Exchange Server ou SharePoint Server exposées publiquement.

---
[Source](https://thehackernews.com/2025/08/microsoft-discloses-exchange-server.html){:target="_blank"}
