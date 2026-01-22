---
title: 'ThreatsDay Bulletin: Pixel Zero-Click, Redis RCE, China C2s, RAT Ads, Crypto Scams & 15+ Stories'
date: 2026-01-22
permalink: /posts/2026/01/22/threatsday-bulletin-pixel-zero-click-redis-rce-china-c2s-rat-ads-crypto-scams-15-stories/
tags:
- veille-cyber
- hackernews
---
## Vigilance Technologique : Vulnérabilités et Stratégies d'Attaque Actuelles

Les menaces récentes, loin de recourir à des méthodes inédites, exploitent des systèmes familiers et des processus routiniers, rendant l'accès aux attaquants particulièrement aisé. L'accent est mis sur la discrétion, la patience et l'abus de confiance plutôt que sur la rapidité spectaculaire.

### Points Clés et Vulnérabilités

*   **Campagnes de Spear-Phishing:** Des courriels ciblés utilisent de faux documents administratifs pour distribuer des backdoors, comme dans le cas de l'Opération Nomad Leopard visant des entités gouvernementales afghanes.
*   **Attaques par Déni de Service (DoS):** Des groupes hacktivistes, notamment pro-russes, perturbent les services critiques et les organisations gouvernementales au Royaume-Uni.
*   **Chargement de DLL Malveillantes:** Des exécutables de confiance sont détournés pour charger des bibliothèques DLL malveillantes (DLL side-loading), permettant l'exfiltration de données. Des archives ZIP imitant des installateurs légitimes sont utilisées pour la distribution.
*   **Abus du Sous-système Windows pour Linux (WSL):** Une technique permet d'interagir avec WSL sans lancer le processus `wsl.exe`, autorisant la liste des distributions et l'exécution de commandes arbitraires.
*   **Publicités Trompeuses:** Des annonces pour des outils de conversion malveillants distribuent des RAT (Remote Access Trojans) persistants.
*   **Certificats TLS à Courte Durée:** Let's Encrypt généralise la disponibilité de certificats TLS d'une durée de vie de 6 jours, opt-in.
*   **Utilisation Abusive des Tickets de Support:** Des systèmes de support non sécurisés, comme Zendesk, sont transformés en vecteurs de spam grâce à la génération automatique d'e-mails de confirmation.
*   **Nouvelle Législation Cyber de l'UE:** La Commission Européenne propose une loi visant à exclure les fournisseurs à haut risque pour sécuriser les réseaux de télécommunications et les infrastructures critiques.
*   **Scans Massifs de Plugins WordPress:** Une activité de reconnaissance à grande échelle vise à identifier les plugins WordPress potentiellement vulnérables, notamment Post SMTP, Loginizer, LiteSpeed Cache, SEO by Rank Math, Elementor et Duplicator.
*   **Vulnerabilités dans les Paquets Rust (Crates):** Crates.io intègre un onglet "Sécurité" pour afficher les avis de sécurité provenant de la base de données RustSec. Le mode "Trusted Publishing" bloque les déclencheurs GitHub Actions risqués.
*   **Infrastructure de Commandement et Contrôle (C2) en Chine:** Plus de 18 000 serveurs C2 sont hébergés en Chine, utilisés principalement pour des botnets IoT (Mozi), Cobalt Strike, Vshell et Mirai.
*   **Espionnage Militaire Présumé:** Un ancien consultant IT des Forces armées suédoises est détenu pour suspicion de transmission d'informations à la Russie.
*   **Vulnérabilités Critiques dans la Plateforme d'une Chaîne d'Approvisionnement:** Des failles (CVE-2026-22236 à CVE-2026-22240) dans la plateforme Bluvoyix de Bluspark Global auraient pu permettre un contrôle total de la plateforme et l'accès aux données clients.
*   **Arnaques aux Cryptomonnaies à Grande Échelle:** Les escroqueries aux cryptomonnaies ont rapporté 14 milliards de dollars en 2025, avec une augmentation significative des escroqueries par impersonation et "pig butchering", utilisant de plus en plus l'IA et les deepfakes.
*   **Démantèlement d'un Réseau de Malware pour DAB:** Un groupe de Vénézuéliens a plaidé coupable pour des vols à l'aide de malwares visant des distributeurs automatiques de billets (DAB) aux États-Unis.
*   **Exploit "Zero-Click" sur Pixel:** Un exploit "zero-click" exploite le décodeur audio Dolby et des vulnérabilités (CVE-2025-54957, CVE-2025-36934) pour compromettre des smartphones Android via l'application Google Messages, permettant l'exécution de code arbitraire et l'escalade de privilèges.
*   **Publicités Malveillantes Distribuant un Infostealer:** Une campagne de malvertising utilise Google Ads pour distribuer un éditeur de PDF falsifié qui installe l'infostealer TamperedChef, connu pour sa latence d'exécution.
*   **Fichiers PNG Cachant un JS Stealer:** Des archives ZIP contenant des factures pharmaceutiques falsifiées mènent au téléchargement d'un script JavaScript qui, via PowerShell, télécharge une image PNG modifiée contenant un chargeur de malware (VMDetectLoader) et le PureLogs Stealer.
*   **Offres de Prêt Trompeuses:** Une campagne de phishing à grande échelle au Pérou utilise de fausses offres de prêt diffusées sur les réseaux sociaux pour collecter des données personnelles et bancaires sensibles.
*   **Installation de Proxyware via un Installateur Falsifié:** Un faux installateur Notepad++ est utilisé pour distribuer du proxyware en Corée du Sud, monétisant la bande passante internet inutilisée des victimes.

### Recommandations

*   **Prudence accrue face aux communications non sollicitées:** Examiner attentivement les e-mails, les documents et les liens, même s'ils semblent provenir de sources légitimes.
*   **Mises à jour régulières des logiciels et systèmes:** Appliquer rapidement les correctifs de sécurité pour les systèmes d'exploitation, les applications, les plugins et les bibliothèques logicielles.
*   **Vérification des sources de téléchargement:** Télécharger les logiciels uniquement à partir de sites officiels et fiables.
*   **Sensibilisation aux tactiques d'ingénierie sociale:** Être vigilant face aux campagnes de phishing, aux escroqueries et aux offres trop belles pour être vraies, notamment dans le domaine des cryptomonnaies et des prêts.
*   **Renforcement de la sécurité des systèmes de support:** Configurer les plateformes de support pour n'accepter que les soumissions d'utilisateurs vérifiés et supprimer les placeholders de déclencheurs de première réponse.
*   **Surveillance des dépendances logicielles:** Utiliser les outils disponibles pour vérifier la sécurité des bibliothèques (crates) avant leur intégration.
*   **Prudence avec les infrastructures cloud et les fournisseurs tiers:** Tenir compte des réglementations de sécurité, comme la nouvelle législation européenne, et évaluer les risques liés aux fournisseurs externes.
*   **Sécurisation des appareils personnels et professionnels:** Être attentif aux exploits "zero-click" et aux techniques d'exécution furtive de logiciels malveillants.
*   **Utilisation d'un réseau privé virtuel (VPN) et de mesures de sécurité supplémentaires:** Particulièrement lors de l'utilisation de réseaux publics ou pour protéger la vie privée lors de transactions en ligne.

---
[Source](https://thehackernews.com/2026/01/threatsday-bulletin-pixel-zero-click.html){:target="_blank"}
