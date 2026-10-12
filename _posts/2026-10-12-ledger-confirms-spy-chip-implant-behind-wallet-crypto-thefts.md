---
title: 'Ledger confirms spy chip implant behind wallet crypto thefts'
date: 2026-10-12
permalink: /posts/2026/10/12/ledger-confirms-spy-chip-implant-behind-wallet-crypto-thefts/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission matérielle : Puces espionnes dans les portefeuilles Ledger

Des dispositifs Ledger compromis ont été identifiés, principalement via le revendeur malaisien « CryptoBilis ». Ces appareils ont été modifiés physiquement par l'ajout d'une puce espionne matérielle permettant le vol de cryptomonnaies.

**Points clés :**
*   **Mode opératoire :** L'implant intercepte l'affichage et les saisies clavier pour dérober la phrase de récupération (seed phrase). Les données sont ensuite transmises aux attaquants via une connexion LTE intégrée utilisant une eSIM.
*   **Technique :** Les dispositifs, indétectables par les logiciels de vérification classiques, utilisent des composants électroniques miniaturisés (MCU, module LTE) dissimulés sous la batterie ou l'écran du Ledger Nano X.
*   **Origine :** Les attaques ciblent spécifiquement les unités vendues par des canaux non officiels, souvent proposés à des prix très attractifs. 
*   **Vulnérabilité :** Aucune CVE n'est associée, car il s'agit d'une **vulnérabilité physique par intrusion matérielle (Supply Chain Attack)**. Le mécanisme de « Genuine Check » de Ledger ne peut pas détecter ces implants, car l'élément sécurisé (Secure Element) d'origine reste intact.

**Recommandations :**
*   **Achat :** Achetez exclusivement vos portefeuilles matériels sur le site officiel de Ledger ou auprès de revendeurs officiellement agréés.
*   **Précaution immédiate :** Si vous avez acheté un appareil auprès d'un revendeur non autorisé ou suspect, ne l'utilisez pas.
*   **Action corrective :** Si l'appareil a déjà été configuré, considérez que vos clés privées sont compromises. Transférez immédiatement vos fonds vers un nouveau portefeuille matériel légitime généré avec une nouvelle phrase de récupération (seed phrase).
*   **Vigilance :** Inspectez physiquement le matériel en cas de doute (présence de fils suspects, antenne ou composants non documentés).

---
[Source](https://www.bleepingcomputer.com/news/security/ledger-confirms-hardware-wallet-spy-implant-behind-crypto-thefts/){:target="_blank"}
