---
title: 'Telegram Android Flaw Lets Attackers Run Code When Users Answer Voice Calls'
date: 2026-10-29
permalink: /posts/2026/10/29/telegram-android-flaw-lets-attackers-run-code-when-users-answer-voice-calls/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans les appels Telegram pour Android

Une faille de sécurité dans l'application Telegram pour Android permet à un attaquant de prendre le contrôle total d'un appareil via un appel vocal. En enchaînant cette vulnérabilité avec deux autres bugs, un attaquant peut s'extraire de l'application, obtenir les privilèges root et accéder aux données sensibles (messages, microphone, caméra).

**Points clés :**
*   **Vecteur d'attaque :** La faille est déclenchée lorsqu'une victime accepte un appel vocal Telegram provenant d'un compte ordinaire.
*   **Cause technique :** Le problème réside dans la gestion des messages de signalisation `MediaState` au sein de la bibliothèque `tgcalls`. Le code accédait de manière erronée à des zones mémoire non autorisées en raison d'une mauvaise gestion des champs manquants lors du traitement de la rotation vidéo.
*   **Portée :** Affecte les versions de Telegram pour Android comprises entre 8.6.2 et 12.10.3.
*   **Statut :** Aucune identification CVE n'a été attribuée à ce jour, Telegram ayant minimisé le risque de l'exécution de code à distance lors du signalement par NebuSec.

**Vulnérabilité associée :**
*   **CVE-2026-111105 :** Faille distincte dans la bibliothèque `rlottie` (utilisée pour les stickers animés) permettant l'exécution de code, bien que son exploitation soit atténuée sur certaines versions.

**Recommandations :**
*   **Mise à jour immédiate :** Passer à la version **12.10.4** ou ultérieure de Telegram pour Android (vérifiable dans les paramètres de l'application).
*   **Mesure de protection temporaire :** Configurer les options de confidentialité des appels sur « Personne » (Nobody) dans les paramètres de Telegram pour empêcher les appels provenant d'inconnus, ou décliner systématiquement les appels suspects.

---
[Source](https://thehackernews.com/2026/10/telegram-android-flaw-lets-attackers.html){:target="_blank"}
