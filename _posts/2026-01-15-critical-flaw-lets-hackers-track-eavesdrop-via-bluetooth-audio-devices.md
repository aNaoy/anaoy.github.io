---
title: 'Critical flaw lets hackers track, eavesdrop via Bluetooth audio devices'
date: 2026-01-15
permalink: /posts/2026/01/15/critical-flaw-lets-hackers-track-eavesdrop-via-bluetooth-audio-devices/
tags:
- veille-cyber
- bleepingcomp
---
**WhisperPair : Un risque de sécurité majeur pour les appareils audio Bluetooth**

Une vulnérabilité critique affectant le protocole Fast Pair de Google expose des centaines de millions d'appareils audio Bluetooth à des risques d'espionnage et de pistage. Cette faille, baptisée WhisperPair (CVE-2025-36911), ne concerne pas les smartphones mais les accessoires audio eux-mêmes, rendant les utilisateurs d'Android comme d'iOS vulnérables.

**Points clés :**

*   **Exploitation du protocole Fast Pair :** De nombreux fabricants n'ont pas correctement implémenté le protocole Fast Pair, permettant à des appareils non autorisés d'initier un appairage sans le consentement de l'utilisateur.
*   **Accès et contrôle :** Une fois l'appairage forcé, un attaquant peut prendre le contrôle total de l'appareil audio, diffusant du contenu audio à fort volume ou écoutant les conversations via le microphone.
*   **Pistage :** La vulnérabilité permet également de pister les utilisateurs via le réseau Find My Hub de Google, en ajoutant l'appareil compromis à son propre compte Google. Les notifications de suivi peuvent être masquées pour l'utilisateur réel.

**Vulnérabilités :**

*   **CVE-2025-36911 (WhisperPair) :** Exploite une faiblesse dans l'implémentation du protocole Fast Pair par les fabricants d'accessoires audio.

**Recommandations :**

*   **Mises à jour du firmware :** La seule défense consiste à installer les mises à jour du firmware fournies par les fabricants d'appareils.
*   **Désactivation de Fast Pair sur Android :** Désactiver la fonction sur les téléphones Android ne résout pas le problème, car la faille réside dans les accessoires.

Google a été informé et a travaillé avec les fabricants pour distribuer des correctifs, mais il est possible que toutes les mises à jour ne soient pas encore disponibles pour tous les appareils vulnérables.

---
[Source](https://www.bleepingcomputer.com/news/security/critical-flaw-lets-hackers-track-eavesdrop-via-bluetooth-audio-devices/){:target="_blank"}
