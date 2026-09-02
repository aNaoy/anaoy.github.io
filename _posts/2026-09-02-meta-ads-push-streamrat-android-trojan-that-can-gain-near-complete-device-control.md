---
title: 'Meta Ads Push StreamRat Android Trojan That Can Gain Near-Complete Device Control'
date: 2026-09-02
permalink: /posts/2026/09/02/meta-ads-push-streamrat-android-trojan-that-can-gain-near-complete-device-control/
tags:
- veille-cyber
- hackernews
---
### StreamRat : Une nouvelle menace Android distribuée via les réseaux sociaux

**Points clés**
*   **Propagation :** Le cheval de Troie bancaire StreamRat a été diffusé via des publicités trompeuses sur Meta (Facebook/Instagram) et TikTok, ciblant des utilisateurs hispanophones avec une fausse application de streaming TV.
*   **Fonctionnement :** Après l'installation d'un fichier APK, le logiciel malveillant utilise un service VPN pour isoler le trafic réseau, contournant ainsi certaines analyses de sécurité.
*   **Capacités :** Une fois les permissions d'accessibilité accordées, les attaquants obtiennent un contrôle quasi total de l'appareil : capture de frappes, vol d'identifiants via des superpositions (overlays), accès à l'interface en temps réel et contrôle à distance.
*   **Lien avec Mirax :** Les chercheurs ont identifié des similitudes techniques et infrastructurelles (GitHub) entre StreamRat et les campagnes précédentes du malware Mirax.

**Vulnérabilités et vecteurs d'attaque**
*   **Vecteur d'entrée :** Sideloading (installation manuelle) d'applications tierces via des liens publicitaires.
*   **Abus de fonctionnalités :** Détournement des API d'accessibilité Android et de `MediaProjection` pour capturer l'écran et simuler des interactions utilisateur.
*   **CVE :** Aucune CVE spécifique n'est associée, car l'attaque repose sur l'ingénierie sociale et l'octroi abusif de permissions système légitimes par l'utilisateur.

**Recommandations**
*   **Éviter le Sideloading :** Ne jamais installer d'applications provenant de sources non officielles, surtout si elles sont proposées via des publicités sur les réseaux sociaux.
*   **Vérifier les permissions :** Suspecter toute application de streaming demandant des accès excessifs (Accessibilité, contrôle de l'écran, VPN ou statut d'application "Home" par défaut).
*   **Surveiller les accès :** Désinstaller immédiatement toute application suspecte ayant obtenu des permissions d'accessibilité.
*   **Hygiène numérique :** Désactiver l'option "Installation à partir de sources inconnues" dans les paramètres de sécurité d'Android.

---
[Source](https://thehackernews.com/2026/09/meta-ads-push-streamrat-android-trojan.html){:target="_blank"}
