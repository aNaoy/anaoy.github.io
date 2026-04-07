---
title: 'Authorities disrupt router DNS hijacks used to steal Microsoft 365 logins'
date: 2026-04-07
permalink: /posts/2026/04/07/authorities-disrupt-router-dns-hijacks-used-to-steal-microsoft-365-logins/
tags:
- veille-cyber
- bleepingcomp
---
### Démantèlement de la campagne FrostArmada : détournement de DNS et vol d'identifiants

Une opération internationale impliquant les autorités (FBI, DOJ, gouvernement polonais) et des acteurs privés (Microsoft, Lumen Black Lotus Labs) a neutralisé **FrostArmada**, une campagne du groupe APT28 (Fancy Bear). Cette opération ciblait principalement des routeurs SOHO (petits bureaux/domicile) pour intercepter des identifiants Microsoft 365 et des jetons OAuth.

**Points clés :**
*   **Mode opératoire :** Les attaquants exploitaient des routeurs exposés sur Internet (MikroTik, TP-Link, certains modèles Fortinet/Nethesis) pour modifier les paramètres DNS.
*   **Technique :** Les requêtes DNS étaient redirigées vers des serveurs VPS contrôlés par les attaquants, agissant comme des proxys *Adversary-in-the-Middle* (AitM).
*   **Impact :** À son apogée en décembre 2025, environ 18 000 appareils étaient compromis dans 120 pays. Les cibles incluaient des agences gouvernementales, des fournisseurs IT et des organisations utilisant leurs propres serveurs.
*   **Signe d'alerte :** La seule indication de compromission pour l'utilisateur était l'affichage d'un avertissement de certificat TLS invalide, souvent ignoré par négligence.

**Vulnérabilités :**
*   L'article ne mentionne pas de CVE spécifique, mais souligne l'exploitation de **routeurs exposés** (surface d'attaque publique) et potentiellement l'utilisation d'équipements en fin de vie (EOL) non patchés.

**Recommandations :**
*   **Gestion des certificats :** Mettre en œuvre l'épinglage de certificats (*certificate pinning*) via une solution MDM pour bloquer les tentatives d'interception.
*   **Réduction de la surface d'attaque :** Appliquer rigoureusement les correctifs de sécurité, limiter l'exposition des interfaces d'administration des routeurs sur le Web et remplacer tout équipement obsolète (EOL).
*   **Vigilance utilisateur :** Ne jamais ignorer les avertissements de sécurité concernant des certificats non fiables lors de connexions à des services critiques.

---
[Source](https://www.bleepingcomputer.com/news/security/authorities-disrupt-dns-hijacks-used-to-steal-microsoft-365-logins/){:target="_blank"}
