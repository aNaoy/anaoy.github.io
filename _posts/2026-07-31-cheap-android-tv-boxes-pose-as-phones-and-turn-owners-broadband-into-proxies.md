---
title: 'Cheap Android TV Boxes Pose as Phones and Turn Owners’ Broadband Into Proxies'
date: 2026-07-31
permalink: /posts/2026/07/31/cheap-android-tv-boxes-pose-as-phones-and-turn-owners-broadband-into-proxies/
tags:
- veille-cyber
- hackernews
---
### Fuyao : Un réseau de fraude publicitaire via des boîtiers Android TV bon marché

Des chercheurs ont découvert une opération malveillante baptisée **Fuyao**, orchestrée par l'entreprise chinoise Zhejiang Fengwo IoT Technology. Cette campagne transforme des boîtiers Android TV économiques en outils de fraude publicitaire à grande échelle et en nœuds de sortie réseau (proxy SOCKS5) à l'insu de leurs propriétaires.

**Points clés :**
*   **Usurpation d'identité :** Les boîtiers sont programmés pour se faire passer pour des smartphones de marques réputées (Samsung, Huawei, Xiaomi, etc.) afin de tromper les systèmes publicitaires.
*   **Mécanisme de fraude :** Une IA basée sur la vision par ordinateur (modèle YOLOv8s) localise et clique automatiquement sur des publicités. Les routines sont générées via une interface de programmation par blocs (Blockly) et exécutées en JavaScript.
*   **Proxy malveillant :** Lorsque le boîtier est inactif (HDMI éteint), il devient un nœud de sortie pour relayer le trafic internet de tiers via la connexion de l'utilisateur.
*   **Échelle :** Plus de 38 000 adresses MAC uniques ont été identifiées en une seule journée, avec un revenu potentiel estimé à plusieurs dizaines de millions de dollars par an.

**Vulnérabilités :**
*   **Absence de certification :** Ces appareils utilisent des firmwares compromis dès la sortie d'usine, sans certification Google Play Protect.
*   **Portes dérobées (Backdoors) :** Utilisation de domaines expirés comme serveurs de commande et de contrôle (C2) pour injecter des profils de périphériques usurpés.
*   *Note : Aucune CVE spécifique n'est associée, car le problème réside dans la conception malveillante native du matériel (Supply Chain Attack).*

**Recommandations :**
*   **Vérification :** Vérifiez si votre appareil est certifié par Google via les paramètres de certification Play Protect.
*   **Isolation :** Déconnectez les appareils de streaming « bon marché » du réseau domestique s'ils présentent un comportement suspect.
*   **Prudence :** Soyez vigilant avec les box Android génériques promettant du contenu gratuit, souvent pré-infectées par des botnets.
*   **Mise à jour :** Maintenez le firmware à jour si cela est possible, bien que ces dispositifs soient souvent laissés sans correctifs par les constructeurs.

---
[Source](https://thehackernews.com/2026/07/cheap-android-tv-boxes-pose-as-phones.html){:target="_blank"}
