---
title: 'Hirudo Android Trojan Uses Patched Banking Apps to Bypass Their Built-In Security Checks'
date: 2026-10-14
permalink: /posts/2026/10/14/hirudo-android-trojan-uses-patched-banking-apps-to-bypass-their-built-in-security-checks/
tags:
- veille-cyber
- hackernews
---
### Hirudo : Une nouvelle menace Android remplaçant vos applications bancaires

Le cheval de Troie bancaire **Hirudo** introduit une méthode d'attaque sophistiquée sur Android : il ne se contente pas de voler des données, il remplace les applications bancaires légitimes par des versions patchées. Cette technique permet aux attaquants de contourner les mécanismes de sécurité internes des banques et de prendre le contrôle total des sessions utilisateur.

**Points clés :**
*   **Propagation :** Le malware se diffuse via des applications « dropper » (shopping, divertissement) téléchargées depuis de faux sites imitant le Google Play Store, souvent relayées par des publicités sur les réseaux sociaux.
*   **Mécanisme de remplacement :** Hirudo détecte l'application bancaire installée, incite l'utilisateur à effectuer une fausse mise à jour, désinstalle l'application réelle et installe simultanément une version modifiée.
*   **Contournement de sécurité :** Les versions patchées intègrent un moteur de « hooking » qui leurre l'application cible. Elles répondent positivement aux contrôles d'intégrité (*Play Integrity*), falsifient la signature numérique et désactivent les protections contre les captures d'écran (suppression du flag `FLAG_SECURE`).
*   **Cibles :** Actuellement identifié pour huit applications bancaires indonésiennes, avec un périmètre de vol d'identifiants couvrant l'Inde, la Chine, le Mexique, le Maroc et la Thaïlande.
*   **Anti-détection :** Utilisation d'un VPN non fonctionnel lors de l'installation pour bloquer l'accès Internet et empêcher les vérifications cloud de Google Play Protect.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur le détournement des fonctionnalités légitimes du système Android (services d'accessibilité) et l'injection de code malveillant dans des applications reconstruites (tampering).

**Recommandations :**
*   **Pour les développeurs d'applications :** Les contrôles de sécurité (signature, intégrité, accessibilité) ne doivent pas reposer uniquement sur les signaux produits localement par l'application, car ceux-ci peuvent être falsifiés. Une vérification côté serveur des données critiques est indispensable.
*   **Pour les utilisateurs :** 
    *   Installer des applications uniquement depuis le Google Play Store officiel et éviter de cliquer sur des publicités suspectes menant à des téléchargements externes.
    *   Se méfier des invites de « mise à jour » inhabituelles qui apparaissent à l'intérieur d'applications tierces.
    *   Ne pas accorder systématiquement les services d'accessibilité, car ils sont le vecteur principal du contrôle à distance par les malwares bancaires.

---
[Source](https://thehackernews.com/2026/10/hirudo-android-trojan-uses-patched.html){:target="_blank"}
