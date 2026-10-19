---
title: 'F5 releases out-of-band patches for critical NGINX vulnerabilities'
date: 2026-10-19
permalink: /posts/2026/10/19/f5-releases-out-of-band-patches-for-critical-nginx-vulnerabilities/
tags:
- veille-cyber
- bleepingcomp
---
# Correctifs critiques pour les vulnérabilités NGINX

F5 a publié des correctifs urgents pour résoudre trois vulnérabilités critiques affectant plusieurs solutions NGINX, notamment NGINX Plus, Open Source, Ingress Controller et Gateway Fabric. Ces failles permettent à des attaquants non authentifiés de provoquer des dénis de service (DoS) ou d'exécuter du code arbitraire sur des configurations spécifiques, via des dépassements de tampon ou des erreurs de type "use-after-free".

### Vulnérabilités identifiées
*   **CVE-2026-15176 & CVE-2026-97205** : Situées dans le module `ngx_http_v3_module`, ces failles peuvent mener à l'exécution de code ou au crash du processus worker NGINX.
*   **CVE-2026-93479** : Affecte la directive `map` de NGINX, permettant potentiellement une exécution de code ou des attaques DoS.

### Points clés
*   **Impact** : Risque d'exécution de code à distance (RCE) si le mécanisme ASLR est désactivé ou contourné.
*   **Menace** : Bien qu'aucune exploitation active ne soit signalée à ce jour, les produits F5 sont des cibles fréquentes pour les groupes de cybercriminels et les acteurs étatiques.

### Recommandations de mitigation
En l'absence d'application immédiate des correctifs, les mesures suivantes sont préconisées :
*   **Pour CVE-2026-15176** : Éviter l'utilisation de la directive `alias` dans les blocs `location` ou de la variable `$request_filename`.
*   **Pour CVE-2026-97205** : Désactiver l'E/S de fichier asynchrone (AIO) ou les Server Side Includes (SSI).
*   **Pour CVE-2026-93479** : Remplacer les captures anonymes par des captures nommées et restreindre leur usage aux blocs contenant la correspondance regex.

---
[Source](https://www.bleepingcomputer.com/news/security/f5-releases-out-of-band-patches-for-critical-nginx-vulnerabilities/){:target="_blank"}
