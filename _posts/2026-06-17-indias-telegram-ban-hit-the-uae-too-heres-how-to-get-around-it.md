---
title: 'Indias Telegram ban hit the UAE too. Heres how to get around it'
date: 2026-06-17
permalink: /posts/2026/06/17/indias-telegram-ban-hit-the-uae-too-heres-how-to-get-around-it/
tags:
- veille-cyber
- bleepingcomp
---
### Blocage de Telegram en Inde : enjeux techniques et contournement

Le gouvernement indien a ordonné le blocage de Telegram jusqu'au 22 juin pour lutter contre la fraude aux examens nationaux (NEET). Cette mesure s'accompagne d'une restriction des fonctionnalités d'édition de messages jusqu'au 30 juin afin d'empêcher la falsification de preuves. L'incident a provoqué des dommages collatéraux, notamment aux Émirats arabes unis, en raison d'une fuite de routage BGP.

**Points clés :**
*   **Fuite de routage (BGP Hijacking) :** L'opérateur indien Reliance (AS18101) a annoncé par erreur les préfixes IP de Telegram, détournant le trafic mondial. Cette anomalie, bien que non intentionnelle selon les experts, a été relayée par FLAG Telecom (AS15412) en raison d'un défaut de validation RPKI.
*   **Controverse sur la proportionnalité :** L'Internet Freedom Foundation (IFF) et Pavel Durov dénoncent une mesure disproportionnée qui pénalise des millions d'utilisateurs légitimes pour les agissements d'une minorité.
*   **Impact opérationnel :** Le blocage a entravé l'accès aux ressources éducatives essentielles pour de nombreux étudiants.

**Vulnérabilités et risques :**
*   **BGP Hijacking :** L'absence de filtrage rigoureux des annonces de routage (RPKI) permet à des erreurs de configuration réseau de provoquer des pannes d'accès internationales.
*   **Confidentialité des proxies :** L'utilisation de proxys tiers pour contourner la censure comporte un risque : l'opérateur du proxy peut journaliser l'adresse IP de l'utilisateur et ses horaires de connexion, même si le chiffrement de bout en bout de Telegram demeure intact.

**Recommandations :**
*   **Contournement via MTProto :** Les utilisateurs peuvent restaurer leur accès en utilisant la fonctionnalité intégrée de "Proxy MTProto" disponible dans les paramètres avancés de l'application Telegram.
*   **Sécurité des proxies :** Il est fortement recommandé d'utiliser des sources de proxys vérifiées et de confiance (ex: projets GitHub communautaires). Pour une protection renforcée, il est conseillé de coupler l'utilisation d'un proxy avec un VPN fiable.
*   **Vigilance réseau :** Les opérateurs télécoms doivent impérativement renforcer la validation des origines de routage (RPKI) pour éviter la propagation mondiale de routes invalides ou détournées.

---
[Source](https://www.bleepingcomputer.com/news/security/indias-telegram-ban-hit-the-uae-too-heres-how-to-get-around-it/){:target="_blank"}
