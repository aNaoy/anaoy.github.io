---
title: 'HTTP/1.1 must die: the desync endgame'
date: 2025-08-07
permalink: /posts/2025/08/07/http11-must-die-the-desync-endgame/
tags:
- veille-cyber
- zerodaysfans
---
## La Fin Inévitable du Protocole HTTP/1.1

Le protocole HTTP/1.1 souffre d'une faille fondamentale qui rend les sites web vulnérables à des détournements de site à grande échelle, exposant des millions d'utilisateurs à la compromission de leurs identifiants. Malgré six années d'efforts d'atténuation, le problème persiste, dissimulé plutôt que résolu.

### Points Clés et Vulnérabilités

*   **Faille Intrinsèque :** HTTP/1.1 manque de délimiteurs de requêtes clairs sur les connexions TCP/TLS sous-jacentes. La présence de multiples méthodes pour spécifier la longueur des requêtes crée une ambiguïté exploitable, permettant à des attaquants de segmenter les requêtes de manière malveillante.
*   **Complexité Cachée :** L'utilisation de proxys inverses et de CDNs, qui redirigent souvent les requêtes HTTP/2 vers HTTP/1.1 en interne, aggrave le problème. Cette transition introduit des complexités supplémentaires et des surfaces d'attaque, comme illustré par une vulnérabilité affectant Cloudflare, qui a involontairement exposé 24 millions de sites.
*   **Nouvelles Classes d'Attaques :** Des techniques inédites de "desync" HTTP, notamment celles basées sur l'en-tête `Expect`, permettent de contourner les défenses existantes. Elles exploitent les divergences dans l'interprétation des longueurs de requête, y compris les scénarios `0.CL` (Content-Length implicite zéro) et `CL.0` (Content-Length à zéro).
*   **Exemples d'Exposition :**
    *   Une vulnérabilité dans l'infrastructure de Cloudflare a involontairement exposé **24 millions de sites** à des détournements de site. (Pas de CVE spécifique mentionné pour cette vulnérabilité Cloudflare).
    *   Des vulnérabilités basées sur l'en-tête `Expect` ont affecté des entreprises comme T-Mobile, GitLab, Netlify et Akamai.
    *   Une vulnérabilité affectant Akamai et liée à l'en-tête `Expect` a été identifiée comme **CVE-2025-32094**. Elle a permis de servir du contenu arbitraire sur `auth.lastpass.com`.

### Recommandations et Stratégies

*   **Abandon de HTTP/1.1 :** La solution à long terme consiste à migrer vers des protocoles plus modernes comme HTTP/2 ou HTTP/3. Ces protocoles, étant binaires et plus stricts dans la gestion des requêtes, éliminent la majorité des vulnérabilités de "desync".
*   **Activer HTTP/2 en Amont :** Pour les proxys et les CDNs, il est crucial d'activer le support HTTP/2 pour les connexions en amont vers les serveurs d'origine.
*   **Mitigation pour HTTP/1.1 :** En attendant la migration complète, les organisations doivent :
    *   Activer toutes les options de normalisation et de validation sur les serveurs frontaux et arrière.
    *   Éviter les serveurs web de niche et privilégier des serveurs éprouvés comme Apache et Nginx.
    *   Effectuer des scans réguliers avec des outils comme "HTTP Request Smuggler".
    *   Envisager de désactiver la réutilisation des connexions en amont si les performances le permettent.
    *   Rejeter les requêtes ayant un corps lorsque la méthode HTTP ne le requiert pas (ex: GET, HEAD).
*   **Sensibilisation :** Une meilleure compréhension de la dangerosité de HTTP/1.1 est essentielle pour encourager son abandon. La publication des découvertes et le partage des techniques sont des étapes importantes.

---
[Source](https://portswigger.net/research/http1-must-die){:target="_blank"}
