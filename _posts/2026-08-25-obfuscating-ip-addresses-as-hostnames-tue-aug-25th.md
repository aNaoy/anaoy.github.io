---
title: 'Obfuscating IP Addresses as Hostnames, (Tue, Aug 25th)'
date: 2026-08-25
permalink: /posts/2026/08/25/obfuscating-ip-addresses-as-hostnames-tue-aug-25th/
tags:
- veille-cyber
- sans-isc
---
### Contournement des listes de blocage par obfuscation DNS

Les attaquants exploitant des vulnérabilités de type SSRF (*Server-Side Request Forgery*) pour cibler le service de métadonnées cloud (169.254.169.254) contournent désormais les systèmes de filtrage par IP en utilisant des noms d'hôtes dynamiques.

**Points clés :**
*   **Obfuscation :** Les attaquants transforment les adresses IP sensibles en noms de domaine via des services comme `nip.io`, `sslip.io` ou des outils spécialisés comme `1u.ms`.
*   **Flexibilité :** L'outil `1u.ms` permet une configuration avancée, incluant le changement dynamique de l'adresse IP de destination après un délai ou un nombre défini de requêtes, facilitant le contournement des défenses basées sur des listes noires (blocklists).
*   **Visibilité :** La nature dynamique de ces requêtes rend la détection inefficace si l'on se contente de filtrer les adresses IP en dur dans le code ou les pare-feu.

**Vulnérabilités :**
*   **SSRF (Server-Side Request Forgery) :** Les applications acceptant des entrées utilisateur pour effectuer des requêtes réseau sont vulnérables si elles ne valident pas correctement les destinations (indépendamment du format : IP ou nom d'hôte).

**Recommandations :**
*   **Ne pas se reposer sur les listes de blocage (blocklists) :** Elles sont insuffisantes face à l'obfuscation DNS.
*   **Surveillance DNS :** Analyser les logs DNS pour identifier les résolutions aboutissant à des adresses sensibles (ex: 169.254.169.254).
*   **Audit d'outils :** Vérifier les logs publics de services comme `1u.ms` pour détecter si votre infrastructure a été ciblée par des requêtes malveillantes.
*   **Renforcement applicatif :** Mettre en œuvre une validation stricte des hôtes et des adresses autorisées au niveau de l'application, plutôt que de simples filtres basés sur des chaînes de caractères.

---
[Source](https://isc.sans.edu/diary/rss/33280){:target="_blank"}
