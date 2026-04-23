---
title: 'Apple Fixes iOS Flaw That Let FBI Recover Deleted Signal Messages'
date: 2026-04-23
permalink: /posts/2026/04/23/apple-fixes-ios-flaw-that-let-fbi-recover-deleted-signal-messages/
tags:
- veille-cyber
- hackernews
---
### Correction de la faille iOS permettant la récupération de messages Signal supprimés

Apple a déployé une mise à jour corrective pour corriger un bug critique dans le service de notifications d'iOS et iPadOS, qui entraînait la conservation indue de données censées être supprimées. Cette vulnérabilité a permis au FBI d'extraire des messages Signal à partir de la base de données des notifications de terminaux saisis, même après la suppression de l'application.

**Points clés :**
*   **Nature du problème :** Un défaut de journalisation dans le service de notifications d'Apple stockait localement le contenu des messages reçus.
*   **Implication légale :** Cette faille a été exploitée par les autorités américaines lors d'investigations judiciaires pour accéder à des communications privées.
*   **Résolution :** Le correctif assure la suppression automatique des notifications conservées par erreur et empêche toute future persistance de données pour les applications supprimées.

**Vulnérabilité :**
*   **CVE-2026-28950 :** Problème de journalisation dans le service de notifications iOS/iPadOS corrigé par une meilleure rédaction des données.

**Recommandations :**
*   **Mise à jour système :** Installer les versions **iOS 26.4.2 / iPadOS 26.4.2** ou **iOS 18.7.8 / iPadOS 18.7.8** (selon le modèle de l'appareil).
*   **Configuration de l'application Signal :** Pour une protection accrue, configurer les paramètres de notification de Signal (Profil > Notifications > Afficher) sur « Nom uniquement » ou « Ni nom ni message » afin de limiter l'exposition du contenu des messages dans l'historique des notifications système.
*   **Gestion des notifications :** Évaluer la nécessité d'activer les notifications pour les applications sensibles afin de réduire la surface d'exposition des données.

---
[Source](https://thehackernews.com/2026/04/apple-patches-ios-flaw-that-stored.html){:target="_blank"}
