---
title: 'OpenSSL HollowByte Flaw Could Freeze Server Memory with 11-Byte TLS Requests'
date: 2026-07-18
permalink: /posts/2026/07/18/openssl-hollowbyte-flaw-could-freeze-server-memory-with-11-byte-tls-requests/
tags:
- veille-cyber
- hackernews
---
### HollowByte : Vulnérabilité de déni de service par épuisement mémoire dans OpenSSL

Une faille critique, baptisée « HollowByte », a été découverte dans OpenSSL. Elle permet à un attaquant de provoquer un déni de service (DoS) par épuisement de la mémoire système en envoyant des requêtes TLS malveillantes de seulement 11 octets.

**Points clés :**
*   **Mécanisme :** Le serveur alloue immédiatement jusqu'à 131 Ko de mémoire vive en se basant sur la taille déclarée dans l'en-tête de la requête, avant même de recevoir le corps du message ou d'effectuer une authentification.
*   **Persistance :** En raison d'une mauvaise gestion de la mémoire par `glibc`, la RAM allouée n'est pas correctement restituée au noyau après la fermeture de la connexion. Les allocations répétées fragmentent le tas et entraînent une augmentation permanente de l'empreinte mémoire du processus, pouvant mener à une interruption du service (OOM-kill).
*   **Opacité :** OpenSSL a corrigé ce bug le 9 juin 2026 sans lui attribuer de CVE, sans publier d'avis de sécurité et sans mentionner la correction dans les journaux de modifications (changelogs).
*   **Étendue :** Le correctif ne concerne que le protocole TLS. La vulnérabilité reste présente dans le code DTLS, que les mainteneurs ont choisi de ne pas corriger pour le moment.

**Vulnérabilité :**
*   **CVE :** Aucune (non répertoriée par OpenSSL).
*   **Versions affectées :** Toutes les versions antérieures aux versions 4.0.1, 3.6.3, 3.5.7, 3.4.6 et 3.0.21.

**Recommandations :**
*   **Mise à jour :** Mettre à jour OpenSSL vers l'une des versions corrigées (4.0.1, 3.6.3, 3.5.7, 3.4.6 ou 3.0.21).
*   **Vérification :** Pour les distributions utilisant le rétroportage (backporting), vérifier auprès du mainteneur du paquet si le correctif spécifique (indiqué dans les *pull requests* 30792, 30793 ou 30794 d'OpenSSL) a été appliqué.
*   **Redémarrage :** Un redémarrage complet des services utilisant OpenSSL est indispensable pour libérer la mémoire fragmentée.

---
[Source](https://thehackernews.com/2026/07/openssl-hollowbyte-flaw-could-freeze.html){:target="_blank"}
