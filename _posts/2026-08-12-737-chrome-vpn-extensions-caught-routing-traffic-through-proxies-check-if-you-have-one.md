---
title: '737 Chrome VPN Extensions Caught Routing Traffic Through Proxies. Check If You Have One'
date: 2026-08-12
permalink: /posts/2026/08/12/737-chrome-vpn-extensions-caught-routing-traffic-through-proxies-check-if-you-have-one/
tags:
- veille-cyber
- hackernews
---
### Vague de maliciels sur le Chrome Web Store : VPN frauduleux et extensions persistantes

Une campagne malveillante a été identifiée sur le Chrome Web Store, impliquant 737 extensions de type VPN ou proxy. Ces outils, ciblant principalement les utilisateurs russophones, usurpent l'identité de marques reconnues (Proton VPN, NordVPN, etc.) pour détourner le trafic web via une infrastructure proxy contrôlée par un acteur unique.

**Points clés :**
* **Détournement de trafic :** Les extensions forcent l'intégralité du trafic du navigateur à transiter par un serveur SOCKS5 (port 1082), plaçant l'attaquant dans une position d'intercepteur (AitM).
* **Usurpation massive :** Sur les 737 extensions, 274 se font passer pour des services VPN légitimes.
* **Techniques de dissimulation :** Utilisation de fausses interfaces de connexion, contournement des politiques de validation de Google et ajout de fonctionnalités malveillantes après approbation.
* **Persistance :** Parallèlement, d'autres extensions comme « AI Sidebar » exploitent des mises à jour légitimes pour réintroduire des mécanismes de monétisation frauduleux (redirections vers des liens affiliés) après avoir été supprimées pour vol de données.

**Vulnérabilités :**
* Aucune CVE spécifique n'est listée, car il s'agit d'une exploitation abusive de l'API `chrome.proxy.settings` et de failles dans le processus de validation du Chrome Web Store. La menace repose sur le détournement volontaire de trafic réseau via une configuration proxy non autorisée par l'utilisateur.

**Recommandations :**
* **Audit des extensions :** Passer en revue les extensions VPN installées sur Chrome. En cas de doute, désinstaller immédiatement toute extension dont l'origine n'est pas vérifiée ou qui ne provient pas du site officiel du fournisseur VPN.
* **Vigilance :** Se méfier des extensions proposant des services « Premium » gratuits ou affichant un comportement incohérent (connexions qui échouent systématiquement, interface trop simple).
* **Sécurité du navigateur :** Privilégier les applications de bureau VPN officielles téléchargées depuis les sites web des éditeurs plutôt que des extensions de navigateur, souvent moins sécurisées.
* **Mise à jour :** Maintenir le navigateur à jour et surveiller les comportements inhabituels après chaque mise à jour automatique des extensions.

---
[Source](https://thehackernews.com/2026/08/737-chrome-vpn-extensions-caught.html){:target="_blank"}
