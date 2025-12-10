---
title: 'New Spiderman phishing service targets dozens of European banks'
date: 2025-12-10
permalink: /posts/2025/12/10/new-spiderman-phishing-service-targets-dozens-of-european-banks/
tags:
- veille-cyber
- bleepingcomp
---
**La menace Spiderman : Une campagne de phishing sophistiquée s'attaque aux banques européennes**

Un nouveau service de phishing nommé Spiderman sévit actuellement en Europe, ciblant des dizaines de banques et de services de cryptomonnaies. Ce kit de phishing permet aux cybercriminels de créer des répliques extrêmement fidèles de sites légitimes pour dérober des informations sensibles.

**Points Clés :**

*   **Portée étendue :** Spiderman vise de nombreuses institutions financières dans cinq pays européens, incluant des enseignes majeures comme Deutsche Bank, ING, CaixaBank, Volksbank, Commerzbank, ainsi que des services fintech tels que Klarna et PayPal.
*   **Vol d'informations critiques :** La plateforme est capable de capturer les identifiants de connexion, les codes d'authentification à deux facteurs (2FA), les données de cartes bancaires et même les phrases de récupération (seed phrases) pour les portefeuilles de cryptomonnaies (Ledger, Metamask, Exodus).
*   **Techniques avancées :** Spiderman excelle dans l'interception en temps réel des codes PhotoTAN, un système d'authentification couramment utilisé par les banques européennes.
*   **Modularité et évolutivité :** La conception modulaire du kit permet d'ajouter facilement de nouvelles banques, portails et méthodes d'authentification, le rendant adaptable aux évolutions des systèmes bancaires en ligne.
*   **Communauté active :** Ce service est populaire auprès des cybercriminels, avec une communauté comptant près de 750 membres sur Signal.
*   **Outils de ciblage sophistiqués :** Les opérateurs peuvent configurer finement leurs cibles par pays, autoriser certains fournisseurs d'accès à Internet (ISP), filtrer par type d'appareil (mobile ou bureau) et rediriger les visiteurs non qualifiés.
*   **Conséquences graves :** Les données volées peuvent mener à la prise de contrôle de comptes bancaires, à la fraude à la carte bancaire, au SIM swapping et à l'usurpation d'identité.

**Vulnérabilités :**

*   Les vulnérabilités exploitées ne sont pas spécifiques à des CVE mais résident dans l'ingénierie sociale et la capacité du kit à simuler parfaitement des interfaces légitimes, trompant ainsi la vigilance des utilisateurs. La capture des codes PhotoTAN représente une vulnérabilité particulière pour les systèmes d'authentification européens.

**Recommandations :**

*   **Vérification systématique des URL :** Toujours s'assurer d'être sur le domaine officiel avant de saisir des identifiants.
*   **Prudence avec les fenêtres "browser-in-the-browser" :** Être vigilant face aux fenêtres d'authentification qui pourraient afficher une URL légitime mais être une simulation.
*   **Signalement des alertes d'authentification :** Toute réception de SMS ou de demande PhotoTAN non initiée par l'utilisateur doit être immédiatement signalée à la banque.
*   **Éducation et sensibilisation :** Informer les utilisateurs sur les techniques de phishing et les risques associés.

---
[Source](https://www.bleepingcomputer.com/news/security/new-spiderman-phishing-service-targets-dozens-of-european-banks/){:target="_blank"}
