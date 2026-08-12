---
title: 'Hundreds of fake Chrome VPN extensions route traffic through a proxy'
date: 2026-08-12
permalink: /posts/2026/08/12/hundreds-of-fake-chrome-vpn-extensions-route-traffic-through-a-proxy/
tags:
- veille-cyber
- bleepingcomp
---
### Vague de fausses extensions VPN sur le Chrome Web Store

Plus de 737 extensions malveillantes ont été identifiées sur le Chrome Web Store, se faisant passer pour des services VPN et proxy légitimes (tels que NordVPN, Proton VPN ou ExpressVPN). Cette campagne a totalisé près de 75 000 téléchargements, ciblant principalement des utilisateurs russes cherchant à contourner des restrictions géographiques.

**Points clés :**
*   **Méthode :** Les extensions détournent tout le trafic Web de l'utilisateur vers des proxies SOCKS5 contrôlés par un unique acteur malveillant (via le port 1082).
*   **Risques :** L'attaquant est en position d'intercepter les destinations visitées, les valeurs SNI TLS, les adresses IP réelles des victimes et les données transmises via HTTP non chiffré.
*   **Fraude :** Certaines extensions proposent de faux abonnements "premium" pour des serveurs inexistants dans divers pays.
*   **Dissimulation :** Les attaquants utilisent des techniques pour masquer les noms de domaine des proxies via des services DNS-over-HTTPS (Cloudflare/Google) et ajoutent des configurations distantes après validation sur le Store.

**Vulnérabilités :**
Aucune CVE spécifique n'est associée à cette campagne, car il s'agit d'une exploitation détournée des fonctionnalités légitimes de l'API des extensions Chrome (configurations proxy forcées) combinée à de l'ingénierie sociale.

**Recommandations :**
*   **Audit immédiat :** Vérifier les extensions installées et supprimer toute extension suspecte identifiée comme faisant partie de cette campagne.
*   **Restauration :** Après désinstallation, s'assurer que les paramètres de configuration proxy de Google Chrome ont été réinitialisés et ne pointent plus vers des serveurs tiers.
*   **Vigilance :** Se méfier des extensions VPN gratuites, particulièrement celles qui usurpent des marques reconnues ou qui demandent des paiements via des interfaces douteuses.

---
[Source](https://www.bleepingcomputer.com/news/security/hundreds-of-fake-chrome-vpn-extensions-route-traffic-through-a-proxy/){:target="_blank"}
