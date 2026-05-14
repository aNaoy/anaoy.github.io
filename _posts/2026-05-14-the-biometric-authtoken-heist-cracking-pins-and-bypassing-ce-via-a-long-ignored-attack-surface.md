---
title: 'The Biometric AuthToken Heist: Cracking PINs and Bypassing CE via a Long-Ignored Attack Surface'
date: 2026-05-14
permalink: /posts/2026/05/14/the-biometric-authtoken-heist-cracking-pins-and-bypassing-ce-via-a-long-ignored-attack-surface/
tags:
- veille-cyber
- zerodaysfans
---
### Vulnérabilité critique du flux d’authentification biométrique Android

Une recherche présentée au *Qualcomm Product Security Summit 2026* met en lumière une surface d'attaque négligée dans le processus d'authentification biométrique d'Android. L'exploitation porte sur la gestion des « AuthTokens », permettant de compromettre la sécurité des données chiffrées de l'appareil.

**Points clés :**
*   **Vecteur d'attaque :** Manipulation des jetons d'authentification (AuthTokens) générés lors de la vérification biométrique.
*   **Impact :** Possibilité de contourner les protections de chiffrement basées sur les identifiants (*Credential Encrypted - CE*) et de déchiffrer des données protégées.
*   **Conséquence secondaire :** La vulnérabilité facilite le cassage de codes PIN (attaques par force brute accélérées ou facilitées par le bypass).

**Vulnérabilités :**
*   L'article ne mentionne pas de CVE spécifique, l'analyse se concentrant sur une faiblesse conceptuelle et structurelle dans l'implémentation de la pile biométrique Android.

**Recommandations :**
*   **Pour les développeurs et constructeurs :** Auditer strictement l'intégrité et le cycle de vie des AuthTokens au sein de l'environnement d'exécution sécurisé (TEE).
*   **Pour les utilisateurs :** Bien que ce type d'attaque nécessite souvent un accès physique ou des privilèges élevés, il est conseillé de maintenir les correctifs de sécurité système à jour dès leur déploiement par les constructeurs.

---
[Source](https://www.darknavy.org/blog/the_biometric_authtoken_heist/){:target="_blank"}
