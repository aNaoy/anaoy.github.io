---
title: 'HTTP/3 in Burp Suite - it’s time to find a bigger wordlist'
date: 2026-09-23
permalink: /posts/2026/09/23/http3-in-burp-suite-its-time-to-find-a-bigger-wordlist/
tags:
- veille-cyber
- zerodaysfans
---
# Optimisation et exploitation des vulnérabilités HTTP/3 avec Burp Suite

La mise à jour de **Turbo Intruder** et l'introduction de l'extension **HTTP/3 Adapter** permettent désormais à Burp Suite de supporter pleinement le protocole HTTP/3, ouvrant la voie à des tests de sécurité à haute performance et à l'exploration de nouvelles surfaces d'attaque.

### Points clés
*   **Performance accrue :** Turbo Intruder atteint désormais plus de 100 000 requêtes par seconde (RPS) via HTTP/3. Le nouveau moteur `AUTO` ajuste dynamiquement les paramètres pour optimiser la vitesse en fonction de l'état du réseau.
*   **Exploitation de conditions de compétition (Race Conditions) :** Intégration de techniques avancées exploitant HTTP/3, telles que le *Single Datagram Attack* et le *QPACK Blocked Streams*, permettant de cibler des fenêtres de vulnérabilité très réduites.
*   **Accès aux cibles exclusives HTTP/3 :** L'extension *HTTP/3 Adapter* convertit le trafic HTTP/1.1 ou HTTP/2 en HTTP/3, rendant testables des services qui étaient jusqu'alors inaccessibles via les outils standards.
*   **Support des attaques par déclassement (Downgrade) :** Possibilité d'injecter des en-têtes via des séquences d'échappement spécifiques pour tester les mécanismes de transition entre HTTP/3 et HTTP/1.

### Vulnérabilités ciblées
L'article met en avant la recherche de vulnérabilités logiques liées aux spécificités du protocole :
*   **Race Conditions (TOCTOU) :** Exploitation des mécanismes de multiplexage de flux HTTP/3 pour contourner les protections classiques contre les conditions de compétition.
*   **HTTP Downgrade Attacks :** Injection de requêtes via des transformations d'en-têtes lors du passage de HTTP/3 vers des protocoles plus anciens, facilitant des attaques de type *Request Smuggling*.
*   *Note : Aucune CVE spécifique n'est mentionnée, ces techniques reposent sur l'exploitation des comportements natifs du protocole.*

### Recommandations
*   **Optimisation des tests :** Pour maximiser le débit lors des tests de fuzzing, privilégier l'utilisation de la méthode `HEAD` ou de l'en-tête `Range` afin de réduire la taille des échanges.
*   **Configuration des moteurs :**
    *   Utiliser le moteur `AUTO` pour des attaques longue durée.
    *   Privilégier le moteur `BURP` (avec réutilisation de connexion désactivée) pour les tests de *desync*.
*   **Diagnostic :** En cas de comportement anormal lors de l'utilisation de l'adaptateur HTTP/3, activer le journal d'échange (`Log exchange to output`) et surveiller l'onglet `Show unsupported origins` pour identifier les échecs de handshake.
*   **Infrastructure :** Pour atteindre des performances maximales (jusqu'à 180 000 RPS), exécuter les tests depuis une instance cloud située dans la même région géographique que la cible.

---
[Source](https://portswigger.net/research/http3-in-burp-suite){:target="_blank"}
