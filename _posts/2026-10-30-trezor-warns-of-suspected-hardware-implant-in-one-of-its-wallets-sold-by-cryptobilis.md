---
title: 'Trezor Warns of Suspected Hardware Implant in One of Its Wallets Sold by CryptoBilis'
date: 2026-10-30
permalink: /posts/2026/10/30/trezor-warns-of-suspected-hardware-implant-in-one-of-its-wallets-sold-by-cryptobilis/
tags:
- veille-cyber
- hackernews
---
### Compromission matérielle de portefeuilles Trezor via le revendeur CryptoBilis

Un signalement récent a révélé la présence d'un circuit électronique malveillant dans un portefeuille matériel *Trezor Safe 5* acquis via le revendeur CryptoBilis. Ce composant non autorisé est conçu pour intercepter et transmettre la phrase de récupération (seed phrase) via un réseau mobile dès que l'appareil est alimenté. Des incidents similaires ont été signalés sur des portefeuilles Ledger provenant du même revendeur, entraînant la fin de leur partenariat avec Trezor.

**Points clés :**
*   **Mode opératoire :** Une carte additionnelle, équipée d'un module cellulaire et d'une antenne, est insérée entre l'écran et la carte mère pour espionner l'affichage des informations sensibles.
*   **Périmètre :** La menace concerne potentiellement tous les modèles Trezor achetés chez CryptoBilis (ou via leurs distributeurs) depuis mars 2026.
*   **Vulnérabilité :** Il n'existe pas de CVE spécifique, car il s'agit d'une altération physique du matériel (supply chain attack) plutôt que d'une faille logicielle.
*   **Risque :** Vol intégral des fonds par exfiltration de la phrase de récupération.

**Recommandations :**
*   **Transfert immédiat :** Si vous avez utilisé un appareil provenant de ce revendeur, transférez vos fonds vers un nouveau portefeuille utilisant une **nouvelle phrase de récupération**. Restaurer l'ancienne phrase sur un autre appareil ne protège pas contre le vol, car celle-ci est déjà compromise.
*   **Ne pas ouvrir l'appareil :** N'essayez pas de vérifier vous-même l'intégrité physique du portefeuille ; contactez le support de Trezor.
*   **Signalement :** Conservez le dispositif compromis et contactez le support officiel de Trezor pour obtenir un remplacement ou un remboursement.
*   **Vigilance accrue :** Soyez attentif aux tentatives de phishing (e-mails, appels) exploitant cette actualité pour usurper l'identité de Trezor ou d'autres services.

---
[Source](https://thehackernews.com/2026/10/trezor-warns-of-suspected-hardware.html){:target="_blank"}
