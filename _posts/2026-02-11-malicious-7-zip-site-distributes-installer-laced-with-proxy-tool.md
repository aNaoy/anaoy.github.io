---
title: 'Malicious 7-Zip site distributes installer laced with proxy tool'
date: 2026-02-11
permalink: /posts/2026/02/11/malicious-7-zip-site-distributes-installer-laced-with-proxy-tool/
tags:
- veille-cyber
- bleepingcomp
---
### Site 7-Zip Falsifié : Une Menace Transformant les PC en Proxies

Une campagne malveillante utilise un site web imitant le site officiel de 7-Zip pour distribuer un installateur compromis. Ce dernier installe discrètement un logiciel qui transforme l'ordinateur de la victime en un nœud de proxy résidentiel. Ces réseaux de proxies permettent de détourner du trafic internet via des appareils domestiques, dans le but de contourner les restrictions, de mener des attaques par credential stuffing, du phishing ou de distribuer d'autres malwares.

Le site frauduleux, 7zip[.]com, a été conçu pour ressembler étroitement à l'original, rendant la tromperie aisée pour les utilisateurs. L'installateur infecté, signé par un certificat révoqué émis à Jozeal Network Technology Co., Limited, contient également une version fonctionnelle de 7-Zip. Cependant, il dépose des fichiers malveillants (Uphero.exe, hero.exe, hero.dll) dans `C:\Windows\SysWOW64\hero\`. Un service Windows est créé pour assurer leur exécution continue, et les règles du pare-feu sont modifiées pour permettre les connexions entrantes et sortantes.

Le malware collecte ensuite des informations sur le système (matériel, mémoire, CPU, disque, réseau) via des APIs Windows et WMI, les transmettant à `iplogger[.]org`. Sa fonction principale est de convertir la machine infectée en un nœud proxy résidentiel, permettant à des tiers de faire transiter leur trafic à travers l'adresse IP de la victime.

La campagne n'est pas limitée à 7-Zip ; des installateurs compromis similaires ont été observés pour d'autres logiciels populaires comme HolaVPN, TikTok, WhatsApp et Wire VPN. La communication avec les serveurs de commande et de contrôle (C2) utilise des domaines rotatifs "smshero" via des connexions HTTPS chiffrées et le protocole DNS-over-HTTPS de Google pour masquer le trafic. Le malware détecte également la présence de plateformes de virtualisation ou de débogueurs pour éviter l'analyse.

**Points clés :**

*   Un faux site 7-Zip distribue un installateur compromis.
*   Le malware transforme les appareils infectés en nœuds de proxy résidentiels.
*   La campagne est plus large et cible plusieurs applications populaires.
*   Le logiciel malveillant tente d'éviter la détection par des analyses et par les défenses réseau.

**Vulnérabilités / Menaces :**

*   **Pas de CVE spécifique mentionné** dans l'article pour cette campagne. La vulnérabilité réside dans l'ingénierie sociale trompant l'utilisateur et dans la capacité du malware à s'installer et à exécuter des fonctions non désirées.

**Recommandations :**

*   **Vérifier la source des téléchargements :** Ne pas télécharger de logiciels à partir de liens trouvés dans des vidéos YouTube ou des résultats de recherche promus.
*   **Utiliser les sites officiels :** Accéder aux sites officiels des logiciels via des favoris ou en tapant manuellement l'adresse pour éviter les sites frauduleux.
*   **Prudence avec les installateurs :** Être vigilant quant aux certificats numériques des exécutables.
*   **Surveillance du trafic réseau :** Les organisations peuvent surveiller les anomalies dans le trafic sortant, bien que les techniques utilisées par ce malware (DoH, ports non standard) rendent cela plus difficile.

---
[Source](https://www.bleepingcomputer.com/news/security/malicious-7-zip-site-distributes-installer-laced-with-proxy-tool/){:target="_blank"}
