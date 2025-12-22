---
title: 'Fake WhatsApp API Package on npm Steals Messages, Contacts, and Login Tokens'
date: 2025-12-22
permalink: /posts/2025/12/22/fake-whatsapp-api-package-on-npm-steals-messages-contacts-and-login-tokens/
tags:
- veille-cyber
- hackernews
---
**Découverte d'un Cheval de Troie dans un Paquet npm pour WhatsApp**

Un paquet malveillant, nommé "lotusbail", a été découvert sur le registre npm. Bien qu'il se présente comme une API fonctionnelle pour WhatsApp, il vole en réalité des messages, des contacts, des tokens de connexion et des fichiers multimédias des utilisateurs. Téléchargé plus de 56 000 fois, ce paquet utilise un wrapper WebSocket pour intercepter les communications et les données sensibles, les transmettant ensuite sous forme chiffrée au serveur de l'attaquant.

De plus, "lotusbail" établit un lien persistant avec le compte WhatsApp de la victime en détournant le processus de couplage d'appareils, conférant ainsi un accès continu même après sa désinstallation. Des capacités anti-débogage sont également intégrées pour détecter et empêcher l'analyse du code malveillant.

**Autres Exploitations dans l'Écosystème Crypto**

Parallèlement, 14 paquets malveillants sur NuGet ont été identifiés, ciblant des outils liés aux cryptomonnaies comme Nethereum. Ces paquets visent à détourner des fonds lors de transactions supérieures à 100 $ ou à voler des clés privées et des phrases de récupération. Ils utilisent des techniques de manipulation des téléchargements et de publication rapide de versions pour gagner la confiance des développeurs. Le paquet "GoogleAds.API" se distingue par son vol d'informations d'authentification OAuth pour les comptes Google Ads, permettant l'usurpation et des dépenses publicitaires frauduleuses.

**Points Clés:**

*   **Nom du Maliciel:** "lotusbail" (paquet npm)
*   **Fonctionnalités Malveillantes:** Vol de messages, contacts, tokens d'authentification, fichiers multimédias ; établissement d'un accès persistant au compte WhatsApp ; fonctionnalités anti-débogage.
*   **Mécanisme d'Attaque:** Wrapper WebSocket malveillant, détournement du processus de couplage d'appareils.
*   **Impact:** Compromission complète du compte WhatsApp, vol de données personnelles et financières.
*   **Paquets NuGet:** 14 paquets malveillants ciblant des outils de cryptomonnaies et Google Ads.
*   **Objectifs des Paquets NuGet:** Détournement de fonds, vol de clés privées, vol d'informations d'authentification OAuth Google Ads.

**Vulnérabilités:**

Aucune CVE spécifique n'est mentionnée dans l'article pour ces cas. Les vulnérabilités exploitées sont liées à la confiance accordée aux dépôts de paquets logiciels (npm, NuGet) et à l'absence de vérification approfondie du code par les développeurs (attaques par la chaîne d'approvisionnement logicielle).

**Recommandations:**

*   **Vigilance Accrue:** Examiner attentivement la source et la réputation des bibliothèques logicielles avant de les intégrer dans des projets.
*   **Analyse Statique et Dynamique:** Effectuer des analyses de sécurité régulières du code des dépendances.
*   **Gestion des Dépendances:** Utiliser des outils de gestion des dépendances qui peuvent détecter les paquets malveillants connus.
*   **Principe de Moindre Privilège:** Accorder aux applications et aux comptes les autorisations strictement nécessaires.
*   **Vérification des Comptes:** Surveiller régulièrement les activités suspectes sur les comptes WhatsApp et les plateformes d'annonces publicitaires.
*   **Mises à Jour de Sécurité:** Maintenir à jour les environnements de développement et les outils pour bénéficier des correctifs de sécurité.

---
[Source](https://thehackernews.com/2025/12/fake-whatsapp-api-package-on-npm-steals.html){:target="_blank"}
