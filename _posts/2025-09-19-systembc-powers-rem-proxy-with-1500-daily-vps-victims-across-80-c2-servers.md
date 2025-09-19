---
title: 'SystemBC Powers REM Proxy With 1,500 Daily VPS Victims Across 80 C2 Servers'
date: 2025-09-19
permalink: /posts/2025/09/19/systembc-powers-rem-proxy-with-1500-daily-vps-victims-across-80-c2-servers/
tags:
- veille-cyber
- hackernews
---
## Le Réseau SystemBC : Une Infrastructure de Proxy Malveillante Puissante

Le malware SystemBC est à l'origine d'un réseau de proxy, REM Proxy, qui fournit une infrastructure significative pour diverses activités malveillantes. Ce réseau compte environ 1 500 victimes quotidiennes réparties sur plus de 80 serveurs de commande et de contrôle (C2). Une proportion notable de ces victimes, près de 80%, sont des serveurs privés virtuels (VPS) compromis, issus de grands fournisseurs commerciaux. Ces VPS sont souvent exploités car ils offrent des capacités de volume et une disponibilité prolongée pour le trafic malveillant, contrairement aux adresses IP résidentielles traditionnelles.

SystemBC, un malware écrit en C, transforme les machines infectées en proxys SOCKS5. Il permet aux hôtes infectés de communiquer avec un serveur C2 et de télécharger des charges utiles supplémentaires. Détecté pour la première fois en 2019, il cible à la fois les systèmes Windows et Linux. Les variantes ciblant Linux semblent particulièrement destinées aux réseaux d'entreprise, aux serveurs cloud et aux appareils IoT.

L'infrastructure du réseau SystemBC est également utilisée par d'autres acteurs malveillants, y compris ceux associés à des groupes de ransomwares comme TransferLoader. De plus, le réseau est utilisé par les propres opérateurs de SystemBC pour mener des attaques par force brute sur les identifiants de sites WordPress, potentiellement pour vendre ensuite ces identifiants compromis à d'autres cybercriminels.

**Points Clés :**

*   **SystemBC :** Malware transformant les machines infectées en proxys SOCKS5.
*   **REM Proxy :** Réseau de proxy alimenté par SystemBC, offrant une infrastructure pour le trafic malveillant.
*   **Victimes :** Environ 1 500 VPS compromis par jour, issus de grands fournisseurs commerciaux.
*   **Serveurs C2 :** Plus de 80 serveurs de commande et de contrôle.
*   **Persistance :** Près de 40% des compromissions ont une durée de vie supérieure à 31 jours.
*   **Diversité des clients :** Utilisé par divers groupes malveillants, y compris des acteurs de ransomwares et des services de scraping web.
*   **Objectif final :** Vente d'identifiants volés et exécution de campagnes malveillantes sur des sites web compromis.

**Vulnérabilités :**

*   Les serveurs victimes, en particulier les VPS, présentent une moyenne de 20 CVE non corrigées, avec au moins un CVE critique par machine.
*   Un VPS identifié était vulnérable à plus de 160 CVE non corrigées.

**Recommandations :**

Bien que l'article ne détaille pas explicitement les recommandations, il met en évidence la nécessité de :

*   **Surveiller et sécuriser les serveurs VPS :** Appliquer les correctifs de sécurité rapidement et régulièrement.
*   **Renforcer les défenses contre le malware SystemBC :** Mettre en place des solutions de sécurité capables de détecter et de bloquer cette menace.
*   **Sécuriser les identifiants :** Utiliser des mots de passe forts et uniques, et envisager l'authentification multifacteur pour les accès aux sites web et aux serveurs.
*   **Surveillance du trafic réseau :** Identifier et bloquer le trafic inhabituel ou suspect émanant des serveurs.

---
[Source](https://thehackernews.com/2025/09/systembc-powers-rem-proxy-with-1500.html){:target="_blank"}
