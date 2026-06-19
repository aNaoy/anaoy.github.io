---
title: 'eBanking Phishing Delivered Through IPv4-Mapped IPv6 Address, (Fri, Jun 19th)'
date: 2026-06-19
permalink: /posts/2026/06/19/ebanking-phishing-delivered-through-ipv4-mapped-ipv6-address-fri-jun-19th/
tags:
- veille-cyber
- sans-isc
---
### Contournement des contrôles de sécurité via des adresses IPv4-mapped IPv6

Une campagne de phishing visant une banque belge utilise une technique d'obfuscation d'URL pour échapper aux filtres de sécurité basés sur des expressions régulières (Regex). L'attaquant insère l'adresse IP du serveur malveillant sous une forme IPv6 mappée en IPv4, rendant l'URL indétectable par les outils recherchant des formats IPv4 standards ou des noms de domaine.

**Points clés :**
*   **Technique d'obfuscation :** Utilisation du format `[::ffff:x.x.x.x]` (représenté en hexadécimal). Dans l'exemple, `[::ffff:5511:74be]` correspond à l'adresse IPv4 `85.17.116.190`.
*   **Absence de DNS :** L'utilisation directe de l'adresse IP dans l'URL élimine le besoin d'enregistrements DNS, rendant la reconnaissance réseau et le blocage par réputation de domaine inopérants.
*   **Méthode d'attaque :** Le lien initial sert de passerelle pour rediriger l'utilisateur vers une page de phishing hébergée sur un domaine tiers (`qzz[.]io`).

**Vulnérabilités :**
*   **Faiblesse des contrôles par Regex :** Les systèmes de filtrage utilisant des expressions régulières simplistes sont incapables de normaliser les différentes représentations d'adresses IP.
*   **Anomalie :** Aucune CVE spécifique n'est associée, il s'agit d'une exploitation de la flexibilité des parsers d'URL (RFC 4291).

**Recommandations :**
*   **Normalisation des URL :** Mettre à jour les outils de sécurité pour qu'ils normalisent systématiquement les adresses IP (conversion IPv6-vers-IPv4) avant toute analyse ou filtrage.
*   **Filtrage par proxy :** Bloquer les connexions directes vers des adresses IP brutes (sans nom de domaine) au niveau du pare-feu ou du proxy web.
*   **Analyse de redirection :** Implémenter une inspection dynamique qui suit les redirections HTTP, car le lien malveillant initial n'est qu'un vecteur de redirection vers le site de phishing final.

---
[Source](https://isc.sans.edu/diary/rss/33090){:target="_blank"}
