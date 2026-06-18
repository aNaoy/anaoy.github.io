---
title: 'F5 Patches Two Critical NGINX Open Source Flaws Enabling Remote Code Execution'
date: 2026-06-18
permalink: /posts/2026/06/18/f5-patches-two-critical-nginx-open-source-flaws-enabling-remote-code-execution/
tags:
- veille-cyber
- hackernews
---
### F5 corrige deux vulnérabilités critiques d'exécution de code à distance dans NGINX

F5 a publié des correctifs de sécurité pour deux vulnérabilités critiques affectant NGINX Open Source et ses dérivés (NGINX Plus, Ingress Controller, etc.). Ces failles permettent à un attaquant distant non authentifié d'exécuter du code arbitraire sur les systèmes ciblés, sous réserve de contourner les protections ASLR.

**Vulnérabilités identifiées :**

*   **CVE-2026-42530 (Score CVSS 9.2) :** Une faille de type *use-after-free* dans le module `ngx_http_v3_module`. Elle peut être exploitée lors de la réouverture d'un flux d'encodage QPACK au sein d'une session HTTP/3 spécifiquement conçue.
*   **CVE-2026-42055 (Score CVSS 9.2) :** Un dépassement de tampon (*buffer overflow*) basé sur le tas dans les modules `ngx_http_proxy_v2_module` et `ngx_http_grpc_module`. Cette vulnérabilité est exploitable dans des configurations spécifiques utilisant HTTP/2 avec les directives `ignore_invalid_headers` réglées sur « off » et `large_client_header_buffers` supérieure à 2 Mo.

**Recommandations :**

*   **Mise à jour immédiate :** Appliquer les correctifs fournis par F5 pour les versions concernées d'NGINX Open Source, Plus, Gateway Fabric, et Ingress Controller (se référer aux bulletins de sécurité F5 pour les versions exactes).
*   **Mesures d'atténuation temporaires :**
    *   Pour **CVE-2026-42530** : Désactiver le protocole HTTP/3.
    *   Pour **CVE-2026-42055** : Passer la directive `ignore_invalid_headers` à « on » ou réduire la taille de la directive `large_client_header_buffers` en dessous de 2 Mo.

---
[Source](https://thehackernews.com/2026/06/f5-patches-two-critical-nginx-open.html){:target="_blank"}
