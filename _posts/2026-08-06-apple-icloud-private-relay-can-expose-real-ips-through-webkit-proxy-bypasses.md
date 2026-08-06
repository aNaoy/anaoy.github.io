---
title: 'Apple iCloud Private Relay Can Expose Real IPs Through WebKit Proxy Bypasses'
date: 2026-08-06
permalink: /posts/2026/08/06/apple-icloud-private-relay-can-expose-real-ips-through-webkit-proxy-bypasses/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité de confidentialité dans iCloud Private Relay via WebKit

Une faille de sécurité découverte dans le moteur WebKit permet de contourner le service « iCloud Private Relay » d'Apple et d'exposer l'adresse IP réelle des utilisateurs. Bien que ce service soit conçu pour masquer l'origine des connexions via une architecture à double relais, certaines fonctionnalités intégrées à WebKit forcent le trafic à sortir directement du réseau local de l'utilisateur, ignorant ainsi la configuration proxy.

**Points clés :**
*   **Impact étendu :** La vulnérabilité touche Safari ainsi que tous les navigateurs tiers utilisant WebKit sur iOS, iPadOS et macOS (Chrome, Firefox, Edge, etc.).
*   **Mécanisme d'exploitation :** Les sites web peuvent exploiter ces fonctionnalités sans aucune interaction de l'utilisateur ni utilisation réelle des passkeys.
*   **Atténuation :** L'utilisation d'un VPN permet de contrecarrer ces fuites, car le trafic est alors encapsulé en dehors du périmètre géré par WebKit.

**Vulnérabilités identifiées :**
Le contournement repose sur trois fonctionnalités de WebKit qui forcent une connexion directe :
*   **DNS Prefetching :** Résout les noms d'hôtes via le DNS local plutôt que par le proxy.
*   **WebAuthn Related Origin Requests :** Force le service d'authentification du système à récupérer des fichiers de validation directement auprès de l'appareil.
*   **WebTransport :** Établit une connexion HTTP/3 directe en ignorant les paramètres de proxy.
*(Note : Aucune CVE n'a été assignée à ce jour pour ces comportements).*

**Recommandations :**
*   **Utilisation d'un VPN :** Pour les utilisateurs nécessitant une confidentialité stricte, l'activation d'un VPN reste la protection la plus efficace contre ces fuites d'IP.
*   **Surveillance :** Les utilisateurs peuvent tester l'intégrité de leur connexion via des outils dédiés comme le site de démonstration « leaks.psylo.app ».
*   **Attente de correctifs :** Apple a confirmé enquêter sur le rapport ; il est conseillé de mettre à jour régulièrement le système d'exploitation et le navigateur dès la disponibilité de correctifs officiels.

---
[Source](https://thehackernews.com/2026/08/webkit-proxy-bypasses-can-expose-real.html){:target="_blank"}
