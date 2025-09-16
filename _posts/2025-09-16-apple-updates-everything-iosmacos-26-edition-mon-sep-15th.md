---
title: 'Apple Updates Everything - iOS/macOS 26 Edition, (Mon, Sep 15th)'
date: 2025-09-16
permalink: /posts/2025/09/16/apple-updates-everything-iosmacos-26-edition-mon-sep-15th/
tags:
- veille-cyber
- sans-isc
---
**Mises à jour de sécurité critiques pour les appareils Apple**

De nombreuses vulnérabilités ont été corrigées dans les dernières mises à jour logicielles d'Apple pour iOS et macOS. Ces failles de sécurité, identifiées par des identifiants CVE, présentent des risques variés allant de l'accès à des données sensibles à la prise de contrôle du système.

**Points Clés et Vulnérabilités identifiées :**

*   **Accès aux données sensibles :** Plusieurs CVE, notamment CVE-2025-24197, CVE-2025-31255, CVE-2025-43190, CVE-2025-43207, CVE-2025-43268, CVE-2025-43292, CVE-2025-43293, CVE-2025-43294, CVE-2025-43303, CVE-2025-43307, CVE-2025-43308, CVE-2025-43311, CVE-2025-43314, CVE-2025-43315, CVE-2025-43317, CVE-2025-43319, CVE-2025-43321, CVE-2025-43325, CVE-2025-43326, CVE-2025-43328, CVE-2025-43337, et CVE-2025-43372, permettent à des applications d'accéder à des informations utilisateur protégées ou sensibles.
*   **Contournement des mesures de sécurité :**
    *   CVE-2025-24088 : une application peut outrepasser les paramètres imposés par MDM.
    *   CVE-2025-30468 : les onglets de navigation privée peuvent être consultés sans authentification via Siri.
    *   CVE-2025-43204, CVE-2025-43286, CVE-2025-43329, CVE-2025-43332, CVE-2025-43340 : des applications peuvent s'échapper de leur bac à sable (sandbox).
    *   CVE-2025-43262 : le mode restreint USB peut ne pas être appliqué aux accessoires connectés au démarrage.
    *   CVE-2025-43304, CVE-2025-43316, CVE-2025-43341, CVE-2025-43298, CVE-2025-43333 : des privilèges root peuvent être obtenus par une application.
    *   CVE-2025-43358 : un raccourci peut contourner les restrictions de sandbox.
*   **Exposition d'informations :**
    *   CVE-2025-24133 : des suggestions du clavier peuvent afficher des informations sensibles sur l'écran de verrouillage.
    *   CVE-2025-43203 : un attaquant avec accès physique à un appareil déverrouillé peut consulter une image dans la note verrouillée la plus récemment consultée.
    *   CVE-2025-43310 : une application peut inciter un utilisateur à copier des données sensibles dans le presse-papiers.
    *   CVE-2025-43357 : une application peut permettre le "fingerprinting" de l'utilisateur.
*   **Exécution de code arbitraire et corruption de mémoire :**
    *   CVE-2025-31254, CVE-2025-43272, CVE-2025-43342, CVE-2025-43343, CVE-2025-43368 : le traitement de contenu web malveillant peut entraîner des redirections inattendues ou des plantages de Safari.
    *   CVE-2025-43277, CVE-2025-43300, CVE-2025-43346, CVE-2025-43372 : le traitement de fichiers audio ou multimédias malveillants peut corrompre la mémoire du processus.
    *   CVE-2025-43287 : le traitement d'images malveillantes peut corrompre la mémoire du processus.
    *   CVE-2025-43353 : le traitement de chaînes de caractères malveillantes peut corrompre la mémoire heap.
*   **Déni de service et instabilité du système :**
    *   CVE-2025-43283, CVE-2025-43302, CVE-2025-43312 : des applications peuvent provoquer une terminaison inattendue du système.
    *   CVE-2025-43295, CVE-2025-43297, CVE-2025-43355 : des applications peuvent provoquer un déni de service.
*   **Problèmes réseau et de communication :**
    *   CVE-2025-31271 : les appels FaceTime entrants peuvent apparaître sur un Mac verrouillé.
    *   CVE-2025-43359 : un socket serveur UDP peut se lier à toutes les interfaces au lieu d'une seule locale.
    *   CVE-2025-43356 : un site web peut accéder aux informations des capteurs sans consentement.
*   **Autres :**
    *   CVE-2025-43300 : Apple est au courant d'un rapport indiquant que cette vulnérabilité relative à ImageIO a été exploitée dans une attaque ciblée.
    *   CVE-2025-43362 : une application peut surveiller les frappes clavier sans permission.
    *   CVE-2025-43366 : une application peut divulguer la mémoire du coprocesseur.

**Recommandations :**

Il est impératif de maintenir tous les appareils Apple à jour avec les dernières versions des systèmes d'exploitation iOS et macOS pour bénéficier des correctifs de sécurité.

---
[Source](https://isc.sans.edu/diary/rss/32286){:target="_blank"}
