---
title: 'Trezor Confirms Hidden Implants in CryptoBilis-Sold Wallets That Can Steal Recovery Phrases'
date: 2026-11-13
permalink: /posts/2026/11/13/trezor-confirms-hidden-implants-in-cryptobilis-sold-wallets-that-can-steal-recovery-phrases/
tags:
- veille-cyber
- hackernews
---
### Compromission matérielle : Implants malveillants sur les portefeuilles Trezor

Trezor a confirmé la présence d'implants matériels malveillants dans des portefeuilles **Trezor Safe 5** vendus par le revendeur **CryptoBilis**. Ces composants ajoutés interceptent les phrases de récupération (seed phrases) et les mots de passe affichés sur l'écran du portefeuille pour les transmettre à des attaquants via un réseau mobile.

**Points clés :**
*   **Modus operandi :** L'implant est un circuit électronique supplémentaire placé entre la carte mère et l'écran. Il copie les données sensibles lors de la création ou de la restauration d'un portefeuille.
*   **Portée :** Le problème concerne spécifiquement les unités Safe 5 achetées auprès de CryptoBilis entre août et septembre 2024. Aucun vol de fonds n'a été signalé à ce jour.
*   **Vulnérabilité :** Il s'agit d'une compromission physique de la chaîne d'approvisionnement. Aucune CVE n'est associée, car la vulnérabilité réside dans l'ajout de matériel tiers (implant) et non dans une faille logicielle du firmware.
*   **Réponse de Trezor :** La mise à jour du firmware 2.13.1 bloque la capacité de l'implant à capturer de nouvelles données sur les appareils déjà compromis, mais ne sécurise pas les phrases de récupération déjà compromises avant la mise à jour.

**Recommandations :**
*   **Transfert immédiat :** Si vous avez acheté un portefeuille chez CryptoBilis depuis mars, déplacez vos fonds vers un nouveau portefeuille généré avec une nouvelle phrase de récupération.
*   **Ne pas réutiliser :** Ne tentez jamais de réutiliser une ancienne phrase de récupération sur un nouveau matériel, car elle doit être considérée comme compromise.
*   **Contact support :** Contactez le support officiel de Trezor pour obtenir un remplacement gratuit si votre appareil provient de ce revendeur.
*   **Prudence physique :** N'essayez pas d'ouvrir ou de démonter votre portefeuille vous-même pour vérifier la présence d'un implant.
*   **Méfiance accrue :** Ne communiquez jamais votre phrase de récupération, même à des entités prétendant offrir des remboursements ou des remplacements.

---
[Source](https://thehackernews.com/2026/11/trezor-confirms-hidden-hardware.html){:target="_blank"}
