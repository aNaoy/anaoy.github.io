---
title: 'Hacking Public Wi-Fi DNS to Steal Credentials'
date: 2026-08-17
permalink: /posts/2026/08/17/hacking-public-wi-fi-dns-to-steal-credentials/
tags:
- veille-cyber
- schneier
---
### Risques et sécurisation des réseaux Wi-Fi publics : l'attaque par détournement DNS

L'utilisation des réseaux Wi-Fi publics expose les utilisateurs à des attaques par détournement DNS. En prenant le contrôle des requêtes DNS, un attaquant peut rediriger le trafic vers des sites malveillants pour intercepter des identifiants. Si l'usage du HTTPS limite cette menace en alertant l'utilisateur via des erreurs de certificat, les attaquants misent sur des sites non sécurisés (HTTP) ou exploitent la négligence des utilisateurs face aux avertissements de sécurité des navigateurs.

**Points clés :**
*   **Vulnérabilité des infrastructures :** Les routeurs publics sont souvent mal configurés ou présentent des vulnérabilités logicielles permettant une compromission DNS.
*   **Interception :** L'attaquant force la résolution de noms de domaine légitimes vers des adresses IP contrôlées par ses soins.
*   **Limites du chiffrement :** Bien que le HTTPS protège contre l'usurpation simple, les attaquants espèrent que les victimes ignoreront les alertes de sécurité des navigateurs ou utiliseront des services HTTP non chiffrés.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, mais l'article pointe des vulnérabilités génériques liées aux **firmwares de routeurs mal sécurisés** et à la dépendance aux serveurs DNS non authentifiés fournis par les points d'accès publics.

**Recommandations :**
*   **Routeur de voyage :** Utiliser un routeur personnel (type GL-iNet sous firmware open-source OpenWRT) pour isoler ses appareils du réseau public.
*   **DNS chiffré et DNSSEC :** Configurer son navigateur ou son routeur pour utiliser des services DNS chiffrés et vérifier la validité DNSSEC pour garantir l'authenticité des sites visités.
*   **Précautions de navigation :** Ne jamais ignorer les avertissements de sécurité des navigateurs concernant les certificats SSL/TLS.
*   **Configuration locale :** Privilégier l'utilisation de résolveurs DNS sécurisés plutôt que ceux imposés automatiquement par le réseau Wi-Fi public.

---
[Source](https://www.schneier.com/blog/archives/2026/08/hacking-public-wi-fi-dns-to-steal-credentials.html){:target="_blank"}
