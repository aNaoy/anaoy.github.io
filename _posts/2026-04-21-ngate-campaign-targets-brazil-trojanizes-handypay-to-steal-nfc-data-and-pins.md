---
title: 'NGate Campaign Targets Brazil, Trojanizes HandyPay to Steal NFC Data and PINs'
date: 2026-04-21
permalink: /posts/2026/04/21/ngate-campaign-targets-brazil-trojanizes-handypay-to-steal-nfc-data-and-pins/
tags:
- veille-cyber
- hackernews
---
### Recrudescence des attaques de relais NFC via l'application HandyPay

Une nouvelle variante du logiciel malveillant **NGate** (aussi appelé NFSkate) cible actuellement les utilisateurs au Brésil en utilisant une version corrompue de l'application légitime **HandyPay**. Ce malware permet aux attaquants de dérober les données NFC des cartes bancaires et le code PIN des victimes pour effectuer des paiements frauduleux ou des retraits aux distributeurs automatiques.

**Points clés :**
* **Mode opératoire :** Les victimes sont incitées à installer une version malveillante de HandyPay via des sites web frauduleux (usurpation d'une loterie d'État ou fausse page de protection bancaire). Une fois installée, l'application demande à devenir l'outil de paiement par défaut.
* **Extraction de données :** L'application incite l'utilisateur à entrer son code PIN et à scanner sa carte bancaire via le capteur NFC du smartphone. Ces données sont ensuite relayées vers les serveurs des attaquants.
* **Utilisation de l'IA :** L'analyse du code suggère l'utilisation de modèles de langage (LLM) pour la génération ou la modification du code malveillant, facilitant ainsi la création de malwares par des acteurs peu qualifiés.
* **Motivation :** Le choix de HandyPay par les cybercriminels est motivé par son coût d'exploitation quasi nul comparé aux solutions « Malware-as-a-Service » (MaaS) classiques, ainsi que par sa discrétion (l'application ne nécessite que peu d'autorisations système).

**Vulnérabilités :**
* Il ne s'agit pas d'une vulnérabilité logicielle spécifique avec un identifiant CVE unique, mais d'un **abus fonctionnel** exploitant la technologie NFC native et l'ingénierie sociale pour détourner une application légitime de ses fonctions initiales.

**Recommandations :**
* **Vigilance sur les sources :** Ne téléchargez jamais d'applications bancaires ou financières en dehors du Google Play Store officiel ou des sites officiels des institutions bancaires.
* **Gestion des permissions :** Soyez extrêmement méfiant envers toute application demandant à devenir l'outil de paiement par défaut sans justification claire.
* **Sensibilisation NFC :** Évitez de rapprocher vos cartes de paiement de votre smartphone à la demande d'applications tierces, particulièrement si celles-ci promettent des gains ou des services inhabituels.
* **Sécurité des terminaux :** Maintenez votre système Android à jour et utilisez des solutions de sécurité mobile reconnues pour détecter les comportements malveillants sur l'appareil.

---
[Source](https://thehackernews.com/2026/04/ngate-campaign-targets-brazil.html){:target="_blank"}
