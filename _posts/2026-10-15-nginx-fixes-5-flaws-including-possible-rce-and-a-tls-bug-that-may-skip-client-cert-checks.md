---
title: 'NGINX Fixes 5 Flaws, Including Possible RCE and a TLS Bug That May Skip Client-Cert Checks'
date: 2026-10-15
permalink: /posts/2026/10/15/nginx-fixes-5-flaws-including-possible-rce-and-a-tls-bug-that-may-skip-client-cert-checks/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques et correctifs de sécurité pour NGINX

NGINX a publié les versions 1.30.6 et 1.31.7 pour corriger cinq vulnérabilités exploitables dans des configurations spécifiques. Bien qu'aucune exploitation active ne soit signalée, ces failles peuvent entraîner des plantages, des corruptions mémoire ou, dans certains cas, une exécution de code arbitraire.

#### Points clés des vulnérabilités

*   **CVE-2026-15176 (Dépassement de tampon) :** Lié à l'usage de `alias` avec `rewrite` ; peut mener à un plantage ou une exécution de code.
*   **CVE-2026-93479 (Dépassement de tampon) :** Concerne l'utilisation de regex `map` avec `root` ou `log_format` ; fait suite à une correction incomplète publiée en juillet.
*   **CVE-2026-97205 (Use-after-free) :** Survient lors de l'utilisation conjointe de `aio` et de pages SSI (`include virtual`).
*   **CVE-2026-95101 (Injection HTTP/3) :** Permet d'injecter des données supplémentaires dans une requête proxifiée via HTTP/3.
*   **CVE-2026-97629 (Faille TLS) :** Erreur dans la rotation automatique des clés de session permettant potentiellement de contourner la vérification des certificats clients.

#### Recommandations

1.  **Mise à jour immédiate :** Passer à la version **1.30.6** (branche stable) ou **1.31.7** (branche mainline).
2.  **Audit de configuration :** Utiliser la commande `nginx -T` pour identifier les directives exposées (telles que `ssl_session_cache shared` sans clé définie, ou l'utilisation combinée d'`aio` et `ssi`).
3.  **Contournements temporaires :** Si une mise à jour est impossible, appliquer les mesures d'atténuation spécifiques fournies par F5 pour chaque configuration vulnérable (par exemple, désactiver `aio` ou configurer explicitement `ssl_session_ticket_key`).
4.  **Produits dérivés :** Les utilisateurs de NGINX Plus, Ingress Controller ou WAF doivent vérifier les avis de sécurité spécifiques à ces produits F5.

---
[Source](https://thehackernews.com/2026/10/nginx-fixes-5-flaws-including-possible.html){:target="_blank"}
