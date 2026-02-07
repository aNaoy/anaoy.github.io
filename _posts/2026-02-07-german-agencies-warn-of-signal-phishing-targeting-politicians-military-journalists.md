---
title: 'German Agencies Warn of Signal Phishing Targeting Politicians, Military, Journalists'
date: 2026-02-07
permalink: /posts/2026/02/07/german-agencies-warn-of-signal-phishing-targeting-politicians-military-journalists/
tags:
- veille-cyber
- hackernews
---
**Campagne de Phishing sur Signal : Ciblage de Hauts Responsables**

Les agences allemandes de sécurité, le BSI et le BfV, alertent sur une campagne de cyberattaques ciblées, probablement d'origine étatique. Celle-ci vise des personnalités politiques, militaires, diplomatiques et des journalistes en Allemagne et en Europe, en utilisant l'application de messagerie Signal.

L'objectif n'est pas de déployer de logiciels malveillants, mais d'exploiter des fonctionnalités légitimes de Signal pour obtenir un accès non autorisé aux conversations et aux listes de contacts des victimes. Les attaquants se font passer pour le "Support Signal" ou un chatbot de sécurité, incitant les cibles à divulguer leur code PIN Signal ou un code de vérification SMS sous peine de perdre leurs données.

Si la victime cède, les attaquants peuvent enregistrer le compte sur un appareil sous leur contrôle, accédant ainsi au profil, aux paramètres, aux contacts et à la liste des blocages. Bien que les conversations passées ne soient pas directement accessibles, ils peuvent intercepter les nouveaux messages et en envoyer en usurpant l'identité de la victime.

Une autre méthode exploitée est la fonction de liaison d'appareils. Les victimes sont trompées pour scanner un code QR, accordant ainsi aux attaquants un accès à leur compte et aux messages des 45 derniers jours sur un appareil contrôlé. Dans ce scénario, les victimes conservent l'accès à leur compte, ignorant que leurs données sont compromises.

Les autorités précisent que cette menace pourrait s'étendre à d'autres applications comme WhatsApp, qui disposent de fonctionnalités similaires de liaison d'appareils et de vérification en deux étapes. Les groupes de menace associés à la Russie, tels que Star Blizzard, UNC5792 et UNC4221, ainsi que des campagnes antérieures comme GhostPairing, sont cités comme ayant mené des attaques similaires.

**Points Clés :**

*   **Cible :** Hauts responsables politiques, militaires, diplomates, journalistes.
*   **Méthode principale :** Phishing sur Signal en se faisant passer pour le support technique.
*   **Objectif :** Vol de codes PIN ou de vérification pour prendre le contrôle de comptes.
*   **Méthode secondaire :** Exploitation de la liaison d'appareils via un QR code piégé.
*   **Impact potentiel :** Accès aux contacts, interception et envoi de messages, compromission potentielle de réseaux via les discussions de groupe.
*   **Extensions possibles :** WhatsApp et autres applications avec des fonctionnalités similaires.
*   **Acteurs suspectés :** Groupes de menace d'origine russe.

**Vulnérabilités (non spécifiques à des CVE, mais des failles fonctionnelles) :**

*   Utilisation de la confiance accordée aux communications "officielles" de support.
*   Ingénierie sociale incitant à la divulgation d'informations sensibles (PIN, codes SMS).
*   Fonctionnalité de liaison d'appareils pouvant être détournée.

**Recommandations :**

*   Ne jamais interagir avec des comptes se présentant comme du support technique et demandant des informations sensibles (PIN, codes).
*   Activer le "Verrouillage d'enregistrement" (Registration Lock) pour empêcher tout enregistrement non autorisé du numéro sur un autre appareil.
*   Vérifier et supprimer périodiquement les appareils liés inconnus.

---
[Source](https://thehackernews.com/2026/02/german-agencies-warn-of-signal-phishing.html){:target="_blank"}
