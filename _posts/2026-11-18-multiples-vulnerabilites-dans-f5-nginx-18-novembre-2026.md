---
title: 'Multiples vulnérabilités dans F5 NGINX (18 novembre 2026)'
date: 2026-11-18
permalink: /posts/2026/11/18/multiples-vulnerabilites-dans-f5-nginx-18-novembre-2026/
tags:
- veille-cyber
- certfr
---
### Vulnérabilités critiques dans F5 NGINX (RCE via HTTP/2)

F5 a émis une alerte concernant deux vulnérabilités critiques affectant NGINX Open Source et NGINX Plus, permettant à un attaquant non authentifié d'exécuter du code arbitraire à distance (RCE) en exploitant le protocole HTTP/2. Une preuve de concept (PoC) est déjà publique pour l'une des failles.

**Points clés :**
*   **Risque :** Exécution de code à distance (RCE).
*   **Vecteur d'attaque :** Protocole HTTP/2.
*   **Vulnérabilités :** CVE-2026-123633 et CVE-2026-123007.

**Systèmes affectés :**
*   **NGINX Open Source :** Versions 1.31.x < 1.31.9 et toutes versions < 1.30.7.
*   **NGINX Plus :** Versions 3.1.x à 3.2.x < 3.7.3.0.1 et versions 3.7.x < 37.0.8.1.

**Recommandations :**
1.  **Application des correctifs :** Mettre à jour NGINX vers les versions sécurisées indiquées dans les bulletins officiels de F5 (K000163926 et K000163928).
2.  **Contournement temporaire :** En attendant la mise à jour, désactivez le support du protocole HTTP/2 dans vos configurations NGINX :
    *   **Versions ≤ 1.25.0 :** Ajoutez la directive `http2 off;` dans le bloc `listen 443 ssl;`.
    *   **Versions > 1.25.0 :** Supprimez le paramètre `http2` du bloc `listen 443 ssl;`.
3.  **Validation :** Appliquez la nouvelle configuration via `sudo nginx -t && sudo nginx -s reload`.

---
[Source](https://www.cert.cyber.gouv.fr/alerte/CERTFR-2026-ALE-017/){:target="_blank"}
