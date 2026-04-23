---
title: 'Apple fixes bug that let the FBI recover deleted Signal messages'
date: 2026-04-23
permalink: /posts/2026/04/23/apple-fixes-bug-that-let-the-fbi-recover-deleted-signal-messages/
tags:
- veille-cyber
- bleepingcomp
---
### Correction d'une faille Apple permettant la récupération de messages Signal supprimés

Apple a déployé des mises à jour de sécurité urgentes pour corriger une vulnérabilité critique affectant le service de notifications d'iOS et iPadOS. Cette faille permettait de conserver en mémoire interne des notifications censées être supprimées, rendant potentiellement accessibles des données privées (telles que des messages Signal) même après leur effacement de l'application ou la suppression de celle-ci.

**Points clés :**
*   Le problème provient du stockage interne des notifications d'Apple plutôt que de l'application Signal elle-même.
*   Des rapports indiquent que cette vulnérabilité a été exploitée par le FBI pour extraire des messages chiffrés à partir de la base de données de notifications d'un iPhone saisi.
*   Apple a amélioré la purge des données pour empêcher cette persistance indésirable.

**Vulnérabilité identifiée :**
*   **CVE-2026-28950 :** Défaut dans le service de notifications entraînant une rétention inappropriée des données après leur suppression.

**Recommandations :**
*   **Mise à jour système :** Installer immédiatement les versions iOS/iPadOS 26.4.2 ou 18.7.8 (et supérieures) pour corriger la faille.
*   **Paramétrage Signal :** Pour limiter les risques de fuite de contenu via les notifications, configurer l'option de contenu des notifications sur « Nom uniquement » ou « Ni nom ni contenu » dans les réglages de l'application Signal.

---
[Source](https://www.bleepingcomputer.com/news/security/apple-fixes-ios-bug-that-retained-deleted-notification-data/){:target="_blank"}
