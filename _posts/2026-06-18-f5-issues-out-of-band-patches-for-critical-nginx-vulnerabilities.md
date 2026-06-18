---
title: 'F5 issues out-of-band patches for critical NGINX vulnerabilities'
date: 2026-06-18
permalink: /posts/2026/06/18/f5-issues-out-of-band-patches-for-critical-nginx-vulnerabilities/
tags:
- veille-cyber
- bleepingcomp
---
### Alert de sécurité : Vulnérabilités critiques sur NGINX

F5 a publié des correctifs d'urgence pour corriger plusieurs failles de sécurité affectant ses solutions NGINX, notamment NGINX Plus, NGINX Open Source, NGINX Gateway Fabric et NGINX Instance Manager. Bien qu'aucune exploitation active ne soit signalée à ce jour, la sévérité des vulnérabilités impose une mise à jour rapide.

**Points clés :**
*   Les failles critiques permettent des attaques par déni de service (DoS) ou l'exécution de code à distance (RCE) sur des configurations spécifiques.
*   Les vecteurs d'attaque reposent sur des mécanismes de *use-after-free* ou de dépassement de tampon (*buffer overflow*).
*   En plus des failles critiques, deux vulnérabilités de haute sévérité affectent NGINX Gateway Fabric, permettant l'injection de directives de configuration arbitraires.

**Vulnérabilités identifiées :**
*   **CVE-2026-42530 (Critique) :** Présente dans `ngx_http_v3_module`.
*   **CVE-2026-42055 (Critique) :** Affecte `ngx_http_proxy_v2_module` et `ngx_http_grpc_module`.
*   **CVE-2026-11311 et CVE-2026-50107 (Haute sévérité) :** Injection de configuration dans NGINX Gateway Fabric.

**Recommandations :**
*   **Mise à jour :** Appliquer immédiatement les correctifs fournis par F5 pour l'ensemble des produits concernés.
*   **Atténuation temporaire (si le patch est impossible) :**
    *   Pour **CVE-2026-42530** : Désactiver HTTP/3 en supprimant `quic` des directives `listen`.
    *   Pour **CVE-2026-42055** : Retirer la directive `ignore_invalid_headers off` et limiter la taille de `large_client_header_buffers` à moins de 2 mégaoctets.

---
[Source](https://www.bleepingcomputer.com/news/security/f5-issues-out-of-band-patches-for-critical-nginx-vulnerabilities/){:target="_blank"}
