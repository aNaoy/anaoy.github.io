---
title: 'TrickMo Android banker adopts TON blockchain for covert comms'
date: 2026-05-11
permalink: /posts/2026/05/11/trickmo-android-banker-adopts-ton-blockchain-for-covert-comms/
tags:
- veille-cyber
- bleepingcomp
---
### Évolution du malware bancaire TrickMo : adoption du réseau TON pour une furtivité accrue

Le cheval de Troie bancaire TrickMo pour Android a franchi une étape critique dans son évolution en intégrant le réseau décentralisé **TON (The Open Network)** pour ses communications de commande et de contrôle (C2). Cette variante, identifiée sous le nom de « Trickmo.C », cible principalement les utilisateurs européens (France, Italie, Autriche) en se dissimulant sous l'apparence d'applications populaires telles que TikTok ou des services de streaming.

**Points clés :**
*   **Infrastructure furtive :** L'utilisation du protocole TON et d'adresses `.adnl` permet de contourner les méthodes classiques de blocage DNS. Le trafic est chiffré et indissociable d'un flux TON légitime, masquant ainsi l'adresse IP réelle des serveurs C2.
*   **Architecture modulaire :** Le malware utilise un chargeur initial (APK) qui télécharge dynamiquement des modules malveillants, facilitant son évolution constante.
*   **Capacités étendues :** Outre le vol de données bancaires, le malware a récemment intégré des outils de réseau avancés (SSH, SOCKS5, `curl`, `telnet`, `traceroute`), transformant les appareils infectés en nœuds de rebond pour les attaquants.
*   **Fonctionnalités malveillantes :** Interception de SMS, enregistrement de frappes (keylogging), capture d'écran, streaming vidéo en direct et contournement des notifications OTP.

**Vulnérabilités :**
*   L'article ne mentionne pas de CVE spécifique, car TrickMo exploite principalement les permissions système légitimes d'Android via l'ingénierie sociale (inciter l'utilisateur à installer des APK malveillants) plutôt que d'exploiter des failles de sécurité logicielles documentées.

**Recommandations :**
*   **Installation restreinte :** Téléchargez uniquement des applications via le Google Play Store officiel.
*   **Hygiène numérique :** Limitez le nombre d'applications installées et privilégiez les éditeurs reconnus et réputés.
*   **Sécurité active :** Maintenez la fonction « Google Play Protect » activée en permanence pour détecter les comportements malveillants sur le terminal.
*   **Vigilance :** Soyez extrêmement méfiant face aux demandes d'installation d'applications provenant de sources tierces ou de liens non sollicités.

---
[Source](https://www.bleepingcomputer.com/news/security/trickmo-android-banker-adopts-ton-blockchain-for-covert-comms/){:target="_blank"}
