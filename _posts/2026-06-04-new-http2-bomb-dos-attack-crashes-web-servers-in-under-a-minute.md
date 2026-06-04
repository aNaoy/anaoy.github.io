---
title: 'New HTTP/2 Bomb DoS attack crashes web servers in under a minute'
date: 2026-06-04
permalink: /posts/2026/06/04/new-http2-bomb-dos-attack-crashes-web-servers-in-under-a-minute/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique : L'attaque "HTTP/2 Bomb"

Une nouvelle technique d'attaque par déni de service (DoS), baptisée « HTTP/2 Bomb », permet de saturer la mémoire vive (RAM) de serveurs web majeurs en quelques secondes à partir d'une seule machine. Cette méthode contourne les mécanismes de défense classiques en exploitant simultanément deux failles de conception du protocole HTTP/2.

**Points clés :**
*   **Fonctionnement :** L'attaque combine l'amplification de compression HPACK (où un octet malveillant génère des milliers d'octets d'allocation mémoire) et le blocage de libération de ressources via des fenêtres de contrôle de flux HTTP/2 à zéro octet.
*   **Efficacité :** Un client unique avec une connexion standard (100 Mbps) peut consommer 32 Go de RAM en moins de 20 secondes sur des serveurs comme Apache ou Envoy.
*   **Impact :** Les serveurs NGINX, Apache HTTP Server, Microsoft IIS, Envoy et Cloudflare Pingora sont exposés.

**Vulnérabilités identifiées :**
*   **CVE-2026-49975 :** Identifiant spécifique attribué à la vulnérabilité corrigée dans Apache httpd (mod_http2 2.0.41).
*   **Vulnérabilités non corrigées :** Aucune mise à jour disponible à ce jour pour Microsoft IIS, Envoy et Cloudflare Pingora.

**Recommandations :**
*   **Mise à jour :** Appliquer les correctifs dès leur disponibilité, notamment pour NGINX (version 1.29.8 et ultérieures) et Apache httpd.
*   **Atténuation immédiate :** Pour les serveurs sans patch (IIS, Envoy, Pingora), il est conseillé de désactiver HTTP/2 si possible.
*   **Protection périmétrique :** Utiliser un pare-feu applicatif (WAF), un reverse proxy ou un CDN devant le serveur pour appliquer des limites strictes sur le nombre d'en-têtes et filtrer les requêtes malveillantes avant qu'elles n'atteignent le serveur.

---
[Source](https://www.bleepingcomputer.com/news/security/new-http-2-bomb-dos-attack-crashes-web-servers-in-under-a-minute/){:target="_blank"}
