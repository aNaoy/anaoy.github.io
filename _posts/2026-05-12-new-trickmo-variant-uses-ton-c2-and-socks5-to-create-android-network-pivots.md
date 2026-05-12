---
title: 'New TrickMo Variant Uses TON C2 and SOCKS5 to Create Android Network Pivots'
date: 2026-05-12
permalink: /posts/2026/05/12/new-trickmo-variant-uses-ton-c2-and-socks5-to-create-android-network-pivots/
tags:
- veille-cyber
- hackernews
---
### Évolution de TrickMo : Le trojan Android utilise le réseau TON pour le pivot réseau

La nouvelle variante du cheval de Troie bancaire Android **TrickMo** (version "TrickMo C") marque une évolution majeure en utilisant le réseau décentralisé **TON (The Open Network)** pour ses communications de commande et contrôle (C2). Cette architecture permet aux attaquants de dissimuler le trafic malveillant et de contrer les efforts de blocage réseau traditionnels.

**Points clés :**
*   **Pivot réseau et proxy SOCKS5 :** Le malware transforme les appareils infectés en nœuds de sortie, permettant aux attaquants de contourner les systèmes de détection de fraude basés sur l'IP pour accéder à des services bancaires ou cryptos.
*   **Reconnaissance réseau :** La nouvelle sous-système réseau intègre des outils tels que `curl`, `dnslookup`, `ping` et `traceroute`, offrant aux pirates des capacités de reconnaissance interne sur les réseaux domestiques ou d'entreprise des victimes.
*   **Infrastructure furtive :** Les communications C2 transitent par des endpoints `.adnl` via un proxy TON local, rendant le trafic difficile à distinguer des activités légitimes.
*   **Distribution :** Le malware se propage via des sites de phishing et des "droppers" déguisés en applications tierces (ex: versions adultes de TikTok), avant de charger dynamiquement le module malveillant (`dex.module`).

**Vulnérabilités exploitées :**
*   **Abus des services d'accessibilité Android :** Utilisés pour intercepter les codes OTP (One-Time Password), enregistrer les frappes clavier, capturer l'écran et permettre une prise de contrôle totale de l'appareil.
*   *Note : Aucune CVE spécifique n'est mentionnée, car le malware repose sur l'abus de fonctionnalités légitimes du système Android.*

**Recommandations :**
*   **Gestion des sources :** Installer uniquement des applications provenant du Google Play Store officiel et désactiver l'option d'installation d'applications de sources inconnues.
*   **Vigilance sur les permissions :** Être extrêmement prudent avec les applications demandant des accès aux "Services d'accessibilité" (Accessibility Services), car il s'agit du vecteur principal de ce type d'attaque.
*   **Sécurité réseau :** Utiliser des solutions de sécurité mobile capables de détecter les comportements anormaux (ex: connexions SOCKS5 inattendues ou trafic réseau persistant via des proxies inhabituels).
*   **Mise à jour :** Maintenir le système d'exploitation Android à jour pour bénéficier des derniers correctifs de sécurité contre les détournements de permissions.

---
[Source](https://thehackernews.com/2026/05/new-trickmo-variant-uses-ton-c2-and.html){:target="_blank"}
