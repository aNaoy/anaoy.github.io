---
title: 'ConsentFix debrief: Insights from the new OAuth phishing attack'
date: 2026-01-14
permalink: /posts/2026/01/14/consentfix-debrief-insights-from-the-new-oauth-phishing-attack/
tags:
- veille-cyber
- bleepingcomp
---
### L'attaque ConsentFix : une nouvelle menace pour les comptes Microsoft

Une nouvelle méthode d'attaque, nommée ConsentFix, a été découverte et neutralisée en décembre. Elle combine des techniques d'ingénierie sociale du type "ClickFix" avec le phishing OAuth pour détourner des comptes Microsoft. Cette campagne à grande échelle s'est propagée via des sites web compromis injectant le code malveillant.

**Points Clés :**

*   **Mécanisme :** L'attaque incite la victime à partager un code d'autorisation OAuth avec l'attaquant via une page de phishing. L'attaquant utilise ensuite ce code pour finaliser le processus d'autorisation sur une application cible de son côté, prenant ainsi le contrôle du compte.
*   **Contournement des sécurités :** ConsentFix contourne les mécanismes d'authentification traditionnels tels que les mots de passe et l'authentification multifacteur (MFA), voire les méthodes résistantes au phishing comme les passkeys, car elle évite le processus d'authentification lui-même.
*   **Ciblage spécifique :** Contrairement aux attaques OAuth classiques qui visent des applications tierces frauduleuses, ConsentFix cible des applications Microsoft de première partie, qui ne peuvent pas être restreintes de la même manière et sont pré-approuvées dans les environnements d'entreprise. Elle exploite également des "scopes" (autorisations) anciens et des exclusions de politiques d'accès conditionnel connues pour échapper à la détection.
*   **Détournement manuel :** L'attaquant effectue manuellement une partie du flux d'autorisation, habituellement géré par l'utilisateur se connectant à des outils comme Azure CLI.
*   **Lien suspecté :** La campagne semble être liée au groupe APT29 affilié à la Russie, utilisant des tactiques furtives. Elle pourrait être une évolution d'une campagne précédente identifiée par Volexity.

**Vulnérabilités et Applications Ciblées :**

ConsentFix exploite des applications de première partie Microsoft qui possèdent des exclusions connues en matière de politiques d'accès conditionnel. Les applications identifiées comme vulnérables incluent :

*   Microsoft Azure CLI (04b07795-8ddb-461a-bbee-02f9e1bf7b46)
*   Microsoft Azure PowerShell (1950a258-227b-4e31-a9cf-717495945fc2)
*   Microsoft Teams (1fec8e78-bce4-4aaf-ab1b-5451cc387264)
*   Microsoft Whiteboard Client (57336123-6e14-4acc-8dcf-287b6088aa28)
*   Microsoft Flow Mobile PROD-GCCH-CN (57fcbcfa-7cee-4eb1-8b25-12d2030b4ee0)
*   Enterprise Roaming and Backup (60c8bde5-3167-4f92-8fdb-059f6176dc0)
*   Visual Studio (872cd9fa-d31f-45e0-9eab-6e460a02d1f1)
*   Aadrm Admin Powershell (90f610bf-206d-4950-b61d-37fa6fd1b224)
*   Microsoft SharePoint Online Management Shell (9bc3ab49-b65d-410a-85ad-de819febfddc)
*   Microsoft Power Query for Excel (a672d62c-fc7b-4e81-a576-e60dc46e951d)
*   Visual Studio Code (aebc6443-996d-45c2-90f0-388ff96faa56)

**Recommandations :**

Face à cette menace, il est crucial d'implémenter des mesures de sécurité avancées :

*   **Activation des journaux :** Assurer l'activation des journaux `AADGraphActivityLogs` (obsolètes mais importants pour cette attaque).
*   **Surveillance des identifiants d'application :** Rechercher dans les journaux les identifiants d'application listés ci-dessus, ainsi que les identifiants des ressources Windows Azure Active Directory (00000002-0000-0000-c000-000000000000) et Microsoft Intune Checkin (26a4ae64-5862-427f-a9b0-044e62572a4f).
*   **Restriction des accès :** Créer des principaux de service pour les applications vulnérables et restreindre les utilisateurs autorisés à y accéder.
*   **Blocage des outils CLI :** Bloquer l'accès aux outils en ligne de commande (CLI) via les politiques d'accès conditionnel, en émettant des exceptions pour les utilisateurs/groupes autorisés.
*   **Surveillance du navigateur :** Surveiller l'activité du navigateur comme surface de détection, chasser les signes d'activités malveillantes et bloquer les attaques en temps réel.
*   **Utilisation de solutions de sécurité dédiées :** Des outils capables de détecter les menaces basées sur le comportement dans le contexte du navigateur sont essentiels pour contrer ce type d'attaques natives au navigateur.
*   **Mise en place de règles de détection :** Utiliser des règles de détection communautaires (par exemple, pour Elastic) et des guides de chasse et d'atténuation.

---
[Source](https://www.bleepingcomputer.com/news/security/consentfix-debrief-insights-from-the-new-oauth-phishing-attack/){:target="_blank"}
