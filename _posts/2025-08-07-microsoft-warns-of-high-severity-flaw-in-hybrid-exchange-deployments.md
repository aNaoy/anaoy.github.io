---
title: 'Microsoft warns of high-severity flaw in hybrid Exchange deployments'
date: 2025-08-07
permalink: /posts/2025/08/07/microsoft-warns-of-high-severity-flaw-in-hybrid-exchange-deployments/
tags:
- veille-cyber
- bleepingcomp
---
### Escalade de Privilèges dans les Déploiements Hybrides Exchange

Un défaut critique affectant les environnements Exchange hybrides permet à des attaquants ayant compromis un serveur Exchange local d'escalader leurs privilèges dans les environnements cloud connectés, tels qu'Exchange Online. Cette vulnérabilité exploite une identité de service partagée, permettant la falsification de jetons ou d'appels API acceptés comme légitimes par le cloud. De plus, les actions malveillantes provenant des serveurs locaux peuvent ne pas être enregistrées dans les journaux de sécurité du cloud, rendant leur détection plus complexe.

**Points Clés:**

*   **Nature de la Vulnérabilité:** Escalade de privilèges dans les déploiements hybrides Exchange.
*   **Mécanisme:** Exploitation d'une identité de service partagée entre les serveurs Exchange sur site et Exchange Online.
*   **Conséquences:** Possibilité de manipuler des jetons ou des appels API pour accéder au cloud, potentiellement sans laisser de traces audibles dans les journaux cloud.
*   **Gravité:** Haute sévérité, avec un risque de compromission totale du domaine hybride.
*   **Produits Affectés:** Exchange Server 2016, Exchange Server 2019, et Microsoft Exchange Server Subscription Edition.
*   **Exploitation:** Bien qu'aucune exploitation en conditions réelles n'ait été observée, le code d'exploitation est considéré comme facile à développer ("Exploitation More Likely").

**Vulnérabilité:**

*   **CVE:** CVE-2025-53786

**Recommandations:**

*   Installer les **Mises à Jour Correctives d'Avril 2025 pour Exchange Server** sur les serveurs Exchange sur site.
*   Suivre les instructions de **déploiement d'une application hybride dédiée Exchange**.
*   Pour les organisations utilisant ou ayant utilisé la configuration hybride, **réinitialiser les clés de sécurité du principal de service** en utilisant le mode de nettoyage du principal de service.
*   Exécuter l'outil **Microsoft Exchange Health Checker** après les corrections pour vérifier si des étapes supplémentaires sont nécessaires.
*   **Déconnecter d'Internet** les serveurs exposés publiquement exécutant des versions obsolètes (fin de vie ou fin de support) d'Exchange Server ou de SharePoint Server.
*   Maintenir les serveurs Exchange sur site à jour avec le dernier **Cumulative Update (CU)**.
*   Migrer vers **Exchange Online** ou mettre à niveau vers **Exchange Server Subscription Edition** pour les versions arrivant en fin de support.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-warns-of-high-severity-flaw-in-hybrid-exchange-deployments/){:target="_blank"}
