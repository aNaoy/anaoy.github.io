---
title: 'Fake AI Chrome extensions with 300K users steal credentials, emails'
date: 2026-02-12
permalink: /posts/2026/02/12/fake-ai-chrome-extensions-with-300k-users-steal-credentials-emails/
tags:
- veille-cyber
- bleepingcomp
---
**Extensions Malveillantes Utilisant l'IA pour le Vol de Données**

Plus de 300 000 utilisateurs ont été ciblés par un ensemble de 30 extensions Chrome malveillantes se présentant comme des assistants IA. Ces extensions détournent les informations de navigation, le contenu des emails et les identifiants des utilisateurs. La campagne, baptisée AiFrame par les chercheurs de LayerX, communique avec une infrastructure centralisée sous le domaine *tapnetic[.]pro*. Certaines de ces extensions, totalisant des centaines de milliers d'installations, sont toujours disponibles sur le Chrome Web Store.

**Points Clés :**

*   **Mascara de l'IA :** Les extensions prétendent offrir des fonctionnalités d'IA, mais redirigent les utilisateurs vers des iframes distantes pour afficher le contenu.
*   **Vol de Données :** Elles collectent des données de pages web visitées, y compris des pages d'authentification sensibles, et ciblent spécifiquement les emails Gmail en accédant au contenu visible et aux brouillons.
*   **Fonctionnalité Vocale Douteuse :** Elles intègrent un mécanisme de reconnaissance vocale et de transcription via l'API Web Speech pour potentiellement intercepter des conversations.
*   **Évasion des Mises à Jour :** L'utilisation d'iframes permet aux opérateurs de modifier la logique des extensions sans déclencher de nouvelle révision par Google, rendant la détection plus difficile.

**Vulnérabilités :**

Bien qu'aucun CVE spécifique ne soit mentionné dans l'article pour ces extensions, le mécanisme de vol de données exploite les permissions accordées par l'utilisateur et l'accès au DOM des pages web. L'utilisation d'iframes distantes ouvre la porte à des modifications de comportement imprévues, similaires à ce qui a été observé avec des modules complémentaires Microsoft Office compromis.

**Recommandations :**

*   Les utilisateurs sont encouragés à consulter la liste des indicateurs de compromission fournie par LayerX pour identifier les extensions suspectes.
*   En cas de suspicion de compromission, il est fortement recommandé de réinitialiser les mots de passe de tous les comptes concernés.
*   Faire preuve de vigilance quant aux extensions installées, surtout celles promettant des fonctionnalités avancées basées sur l'IA, et vérifier attentivement les permissions demandées.

---
[Source](https://www.bleepingcomputer.com/news/security/fake-ai-chrome-extensions-with-300k-users-steal-credentials-emails/){:target="_blank"}
