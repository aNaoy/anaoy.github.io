---
title: 'Windows 11 24H2 updates failing again with 0x80240069 errors'
date: 2025-08-14
permalink: /posts/2025/08/14/windows-11-24h2-updates-failing-again-with-0x80240069-errors/
tags:
- veille-cyber
- bleepingcomp
---
**Mise à jour Windows 11 24H2 : Échec d'installation et erreurs 0x80240069 dans les environnements WSUS**

La récente mise à jour cumulative KB5063878 pour Windows 11 24H2 rencontre des problèmes d'installation pour de nombreux administrateurs système, se manifestant par l'erreur 0x80240069. Ce problème semble affecter spécifiquement les systèmes gérés via Windows Server Update Services (WSUS), où les journaux d'événements indiquent également l'arrêt inattendu du service de mise à jour Windows ("wuauserv").

Bien que Microsoft n'ait pas encore commenté officiellement la situation, une solution temporaire a été partagée par certains administrateurs. Elle consiste à importer manuellement la mise à jour dans WSUS en utilisant des identifiants spécifiques. Ce n'est pas la première fois que des problèmes de déploiement surviennent avec WSUS, des incidents similaires ayant été observés en avril dernier avec des versions antérieures de Windows 11. Microsoft avait alors résolu le problème en mai via un mécanisme de retour en arrière des problèmes connus (KIR).

**Points clés :**

*   La mise à jour cumulative KB5063878 pour Windows 11 24H2 échoue à s'installer.
*   L'erreur rencontrée est 0x80240069.
*   Le problème affecte principalement les utilisateurs de WSUS et les environnements d'entreprise.
*   Des messages d'arrêt du service de mise à jour Windows sont également observés.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article concernant la cause directe de cet échec d'installation. L'article se concentre sur un problème de déploiement de mise à jour plutôt que sur une faille de sécurité exploitée.

**Recommandations :**

*   **Pour les administrateurs utilisant WSUS :**
    *   Tenter d'importer manuellement la mise à jour KB5063878 dans WSUS en utilisant les identifiants suivants :
        *   WSUS Sync : Update-ID 8018eab0-7242-4932-adf2-afda36f6b3f6
        *   Catalog Import : Update-ID 92061378-be93-4659-a72a-037225e6bb0f
    *   Surveiller les communications officielles de Microsoft pour une résolution officielle.
*   **Pour les utilisateurs domestiques :** L'article suggère que les utilisateurs qui ne dépendent pas de WSUS ne devraient pas être affectés par ce problème.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/windows-11-24h2-updates-failing-again-with-0x80240069-errors/){:target="_blank"}
