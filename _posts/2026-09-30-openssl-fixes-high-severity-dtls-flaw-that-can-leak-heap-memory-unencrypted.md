---
title: 'OpenSSL Fixes High-Severity DTLS Flaw That Can Leak Heap Memory Unencrypted'
date: 2026-09-30
permalink: /posts/2026/09/30/openssl-fixes-high-severity-dtls-flaw-that-can-leak-heap-memory-unencrypted/
tags:
- veille-cyber
- hackernews
---
### Correction critique pour la faille DTLS d'OpenSSL

Une vulnérabilité de haute sévérité dans OpenSSL permet une fuite de mémoire du tas (*heap memory*) ou le plantage d'une application utilisant le protocole DTLS. Cette faille survient lors du renvoi de messages de poignée de main (*handshake*) : lorsqu'un envoi est interrompu par une pause dans la communication, le mécanisme de retransmission utilise une position incorrecte dans la mémoire tampon. Cela entraîne l'envoi de données mal étiquetées contenant potentiellement des résidus de mémoire système non chiffrés ou provoque une erreur de lecture mémoire.

**Points clés :**
*   **Impact :** Exposition de données confidentielles (fuite de mémoire) ou déni de service (plantage par accès à une mémoire non mappée).
*   **Contexte :** Concerne les applications utilisant OpenSSL pour les connexions DTLS (ex: WebRTC, appels internet).
*   **Gravité :** Évaluée à 8.2 (CVSS) par la CISA ; OpenSSL la classe comme « Haute ».

**Vulnérabilité :**
*   **CVE-2026-84782**

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs vers les versions suivantes : **4.0.3, 3.6.5, 3.5.9, ou 3.4.8**.
*   **Utilisateurs de versions obsolètes (3.0, 1.1.1, 1.0.2) :** Ces versions ne bénéficient plus de correctifs publics. Il est impératif de migrer vers une branche supportée (ex: 3.5 LTS ou 4.0) ou de souscrire à un support premium pour obtenir les patchs privés.
*   **Distributions Linux :** Les utilisateurs d'Ubuntu ou de Debian doivent mettre à jour leurs paquets système via les gestionnaires de paquets officiels, car ces éditeurs ont publié des correctifs spécifiques pour leurs versions maintenues.

---
[Source](https://thehackernews.com/2026/09/openssl-fixes-high-severity-dtls-flaw.html){:target="_blank"}
