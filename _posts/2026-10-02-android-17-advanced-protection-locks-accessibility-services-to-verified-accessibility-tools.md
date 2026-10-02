---
title: 'Android 17 Advanced Protection Locks Accessibility Services to Verified Accessibility Tools'
date: 2026-10-02
permalink: /posts/2026/10/02/android-17-advanced-protection-locks-accessibility-services-to-verified-accessibility-tools/
tags:
- veille-cyber
- hackernews
---
### Renforcement de la sécurité Android 17 : Limitation des services d'accessibilité

Google renforce la sécurité dans Android 17 en restreignant l'accès à l'API `AccessibilityService` aux seules applications vérifiées et classées comme outils d'accessibilité lorsque le mode « Protection Avancée » est activé. Cette mesure vise à contrer les logiciels malveillants (banking trojans, spywares) qui détournent ces fonctions privilégiées pour intercepter des données sensibles ou effectuer des opérations frauduleuses.

**Points clés :**
*   **Neutralisation des vecteurs d'attaque :** L'API d'accessibilité, conçue pour aider les utilisateurs en situation de handicap, est devenue un vecteur d'attaque majeur. Le mode « Protection Avancée » empêche les applications non légitimes d'en abuser.
*   **Nouvelles fonctionnalités de sécurité sur Android 17 :**
    *   **Intrusion Logging :** Journalisation forensique pour enquêter sur les attaques par spyware.
    *   **USB Protection :** Prévention des accès non autorisés via connexion physique.
    *   **Désactivation WebGPU :** Réduction de la surface d'attaque contre les exploits basés sur le navigateur.
    *   **Failed Authentication Lock :** Verrouillage strict après plusieurs tentatives d'authentification échouées pour contrer le bruteforce.

**Vulnérabilités associées :**
*   **Abus de l'API AccessibilityService :** Bien qu'il ne s'agisse pas d'une CVE unique, l'exploitation de cette API par ingénierie sociale permet aux attaquants d'exécuter des transferts de fonds, d'enregistrer des frappes au clavier, de superposer des interfaces de phishing et de contourner des permissions sans accès root.

**Recommandations :**
*   **Activation de la Protection Avancée :** Les utilisateurs sont encouragés à activer ce mode dans les paramètres système pour restreindre automatiquement les privilèges des applications tierces.
*   **Activation de la journalisation :** Pour une sécurité accrue, activez manuellement l'option « Intrusion Logging » dans les paramètres de Protection Avancée afin de permettre une analyse forensique en cas d'activité suspecte.
*   **Développement :** Les développeurs d'applications doivent utiliser le flag `accessibilityDataSensitive` pour protéger les vues contenant des informations critiques contre les interactions malveillantes.

---
[Source](https://thehackernews.com/2026/10/android-17-advanced-protection-locks.html){:target="_blank"}
