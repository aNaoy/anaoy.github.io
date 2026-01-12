---
title: 'Hidden Telegram proxy links can reveal your IP address in one click'
date: 2026-01-12
permalink: /posts/2026/01/12/hidden-telegram-proxy-links-can-reveal-your-ip-address-in-one-click/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite d'adresse IP via les liens proxy Telegram

Des chercheurs ont démontré qu'il suffisait d'un simple clic sur un lien Telegram apparemment inoffensif pour révéler l'adresse IP réelle d'un utilisateur. Ces liens, souvent déguisés en noms d'utilisateur ou en liens web ordinaires, sont en réalité des liens de configuration de proxy MTProto (commençant par `t.me/proxy?...`).

Lorsque ces liens sont ouverts dans les applications Telegram pour Android et iOS, le client tente automatiquement de se connecter au proxy spécifié. Cette tentative de connexion initie une requête réseau directe depuis l'appareil de l'utilisateur vers le serveur proxy avant même que l'utilisateur n'ait confirmé l'ajout du proxy. Les attaquants peuvent exploiter ce comportement en créant leurs propres serveurs proxy et en distribuant des liens trompeurs. En cliquant sur un tel lien, l'utilisateur expose involontairement son adresse IP au propriétaire du proxy, qui peut ensuite l'utiliser pour le suivi de localisation, des attaques ciblées ou d'autres abus.

Bien que Telegram considère ce comportement comme similaire à celui d'autres services accédant à Internet, l'entreprise ajoutera des avertissements pour les liens proxy afin de sensibiliser davantage les utilisateurs aux liens potentiellement déguisés.

**Points clés:**

*   Les liens proxy Telegram (`t.me/proxy?...`) peuvent être dissimulés derrière des noms d'utilisateur ou des liens ordinaires.
*   Le clic sur ces liens déclenche une connexion de test automatique au proxy spécifié dans les clients Telegram mobile.
*   Cette connexion de test révèle l'adresse IP réelle de l'utilisateur au propriétaire du proxy.
*   L'adresse IP divulguée peut être utilisée pour la localisation, le profilage ou des attaques ciblées.

**Vulnérabilités:**

*   Non spécifié avec un numéro CVE. La vulnérabilité réside dans le mécanisme automatique de test de connexion des liens proxy dans les clients Telegram pour Android et iOS.

**Recommandations:**

*   **Pour les utilisateurs:** Être très prudent avec les liens Telegram, en particulier ceux qui semblent inhabituels ou qui sont reçus de sources non fiables, même s'ils ressemblent à des noms d'utilisateur ou des liens web standards.
*   **Pour Telegram:** L'entreprise a indiqué qu'elle allait ajouter des avertissements pour les liens proxy. Les utilisateurs sont encouragés à attendre l'implémentation de cette fonctionnalité.

---
[Source](https://www.bleepingcomputer.com/news/security/hidden-telegram-proxy-links-can-reveal-your-ip-address-in-one-click/){:target="_blank"}
