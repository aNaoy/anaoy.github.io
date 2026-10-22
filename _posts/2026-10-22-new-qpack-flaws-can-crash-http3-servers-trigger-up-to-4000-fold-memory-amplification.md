---
title: 'New QPACK Flaws Can Crash HTTP/3 Servers, Trigger Up to 4,000-Fold Memory Amplification'
date: 2026-10-22
permalink: /posts/2026/10/22/new-qpack-flaws-can-crash-http3-servers-trigger-up-to-4000-fold-memory-amplification/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques par amplification mémoire dans QPACK (HTTP/3)

Des chercheurs de FoxIO ont découvert des vulnérabilités dans le protocole QPACK d'HTTP/3 permettant à un attaquant non authentifié de provoquer un déni de service (DoS) par épuisement de la mémoire (OOM). En envoyant des en-têtes HTTP malicieusement compressés, l'attaquant force le serveur à décompresser les données en mémoire, créant une amplification pouvant atteindre 4 000 fois la taille initiale.

**Points clés :**
* **Mécanisme :** La vulnérabilité exploite l'absence ou le retard de plafonnement des en-têtes après leur décompression, contrairement à la vérification effectuée sur le flux entrant.
* **Impact :** Crash du serveur, saturation CPU (notamment sur Bun), et blocage des nouvelles requêtes. Aucun vol de données n'a été constaté.
* **Étendue :** Plusieurs bibliothèques HTTP/3 populaires sont affectées, impactant des logiciels comme Caddy, Traefik et les serveurs LiteSpeed.

**Vulnérabilités identifiées :**
* **CVE-2025-64702 :** quic-go (corrigé en v0.57.0)
* **CVE-2026-12523 :** Cloudflare quiche (corrigé en v0.29.3)
* **CVE-2025-13945 :** Wireshark (corrigé en v4.6.2 / 4.4.12)
* **Non référencées :** lsquic (corrigé en v4.9.0), ainsi que les versions non corrigées de **Bun**, **h3 (Rust)** et **aioquic**.

**Recommandations :**
* **Mise à jour :** Appliquer immédiatement les correctifs pour les bibliothèques concernées (quic-go, quiche, lsquic, Wireshark).
* **Atténuation (si correctif indisponible) :**
    * **Bun :** Désactiver l'exposition du serveur HTTP/3.
    * **aioquic/mitmproxy :** Désactiver le support HTTP/3 (`--set http3=false`).
    * **h3 (Rust) :** Configurer manuellement une limite stricte via `max_field_section_size`.

---
[Source](https://thehackernews.com/2026/10/new-qpack-flaws-can-crash-http3-servers.html){:target="_blank"}
