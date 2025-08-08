---
title: 'CISA orders fed agencies to patch new Exchange flaw by Monday'
date: 2025-08-08
permalink: /posts/2025/08/08/cisa-orders-fed-agencies-to-patch-new-exchange-flaw-by-monday/
tags:
- veille-cyber
- bleepingcomp
---
**Urgence de Patching pour Microsoft Exchange : Vulnérabilité Critque Affectant les Environnements Hybrides**

Une faille critique dans Microsoft Exchange, identifiée comme CVE-2025-53786, exige une action immédiate. Les agences fédérales américaines ont reçu l'ordre de la CISA de corriger cette vulnérabilité d'ici lundi.

**Points Clés :**

*   **Impact :** La faille permet à des attaquants possédant des privilèges administratifs sur des serveurs Exchange locaux de se déplacer latéralement vers les environnements cloud de Microsoft. Cela peut mener à une compromission totale du domaine.
*   **Versions affectées :** Microsoft Exchange Server 2016, 2019, et l'Édition d'Abonnement sont concernés.
*   **Détection :** Les outils de journalisation basés sur le cloud, comme Microsoft Purview, pourraient ne pas enregistrer l'activité malveillante provenant d'Exchange sur site, rendant la détection difficile.
*   **Origine :** La vulnérabilité est liée à l'utilisation d'un "service principal" partagé dans les configurations hybrides d'Exchange, une architecture qui a été revue dans le cadre de l'Initiative d'Avenir Sécurisé de Microsoft. Un chercheur en sécurité a démontré cette possibilité d'exploitation lors d'une présentation à Black Hat.

**Vulnérabilités :**

*   **CVE-2025-53786** : Permet le déplacement latéral des environnements on-premises Exchange vers le cloud en exploitant un "service principal" partagé.

**Recommandations et Mesures d'Urgence :**

Les agences fédérales doivent suivre les étapes suivantes :

1.  **Inventaire :** Réaliser un inventaire de leurs environnements Exchange en utilisant le script Microsoft Health Checker.
2.  **Déconnexion des serveurs obsolètes :** Déconnecter les serveurs qui ne sont plus pris en charge par le correctif d'avril 2025.
3.  **Mise à jour et Patching :** Mettre à jour les serveurs restants vers les dernières mises à jour cumulatives (CU14 ou CU15 pour Exchange 2019, CU23 pour Exchange 2016) et appliquer le correctif d'avril 2025.
4.  **Migration vers un Service Principal Dédié :** Exécuter le script PowerShell ConfigureExchangeHybridApplication.ps1 pour passer du service principal partagé à un service principal dédié dans Entra ID.

L'application du correctif seul n'est pas suffisante ; des actions manuelles sont requises pour migrer vers un service principal dédié. L'échec de ces mesures pourrait entraîner une compromission complète des environnements hybrides. La CISA exhorte toutes les organisations, au-delà du secteur fédéral, à appliquer ces correctifs pour se protéger contre cette menace.

---
[Source](https://www.bleepingcomputer.com/news/security/cisa-orders-fed-agencies-to-patch-new-cve-2025-53786-exchange-flaw/){:target="_blank"}
