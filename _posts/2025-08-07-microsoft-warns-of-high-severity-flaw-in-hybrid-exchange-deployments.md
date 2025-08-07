---
title: 'Microsoft warns of high-severity flaw in hybrid Exchange deployments'
date: 2025-08-07
permalink: /posts/2025/08/07/microsoft-warns-of-high-severity-flaw-in-hybrid-exchange-deployments/
tags:
- veille-cyber
- bleepingcomp
---
## Escalade de privilèges dans les environnements Exchange hybrides

Une faille de sécurité critique a été identifiée dans les déploiements Exchange hybrides, permettant potentiellement à des attaquants de gagner des privilèges élevés dans les environnements cloud Exchange Online sans être détectés. Cette vulnérabilité exploite le partage d'une identité de service commune entre les serveurs Exchange locaux et Exchange Online. En contrôlant un serveur Exchange local, un attaquant peut falsifier des jetons ou des appels d'API que le cloud acceptera comme légitimes, car il fait implicitement confiance à l'environnement sur site. De plus, les actions provenant de l'infrastructure locale ne génèrent pas toujours de journaux traçables pour les activités malveillantes dans Microsoft 365, ce qui rend les audits basés sur le cloud potentiellement inefficaces pour détecter de telles intrusions.

### Points clés :

*   Une vulnérabilité d'escalade de privilèges de haute gravité affecte les déploiements Exchange hybrides.
*   Elle permet aux attaquants ayant accès à un serveur Exchange local de compromettre l'environnement cloud connecté.
*   Le manque de journaux d'audit facilement détectables dans le cloud complique la détection des attaques.
*   Une exploitation réussie pourrait mener à une compromission totale du domaine hybride.

### Vulnérabilités :

*   **CVE-2025-53786** : Vulnérabilité d'escalade de privilèges dans les déploiements Exchange hybrides.
    *   Affecte : Exchange Server 2016, Exchange Server 2019, Microsoft Exchange Server Subscription Edition.

### Recommandations :

*   Installer les **mises à jour correctives d'avril 2025 pour Exchange Server** sur les serveurs Exchange locaux.
*   Suivre les instructions de Microsoft pour le **déploiement d'une application hybride dédiée** (Deploy dedicated Exchange hybrid app).
*   Pour les organisations utilisant ou ayant utilisé des configurations hybrides, réinitialiser les `keyCredentials` du principal de service en suivant le guide du **Mode Nettoyage du Principal de Service** (Service Principal Clean-Up Mode).
*   Exécuter le **Microsoft Exchange Health Checker** après les modifications pour vérifier si des étapes supplémentaires sont nécessaires.
*   Déconnecter les serveurs publics exécutant des versions obsolètes (fin de vie ou fin de service) d'Exchange Server ou SharePoint Server d'Internet.
*   Maintenir les serveurs Exchange locaux à jour avec les derniers Cumulative Updates (CU) disponibles.
*   Envisager la migration vers Exchange Online ou la mise à niveau vers Exchange Server Subscription Edition pour les versions arrivant en fin de support.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-warns-of-high-severity-flaw-in-hybrid-exchange-deployments/){:target="_blank"}
