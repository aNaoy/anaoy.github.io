---
title: 'Keystone to Destroy 18,835 Hardware Wallets After Hackers Steal Device Verification Key'
date: 2026-10-27
permalink: /posts/2026/10/27/keystone-to-destroy-18835-hardware-wallets-after-hackers-steal-device-verification-key/
tags:
- veille-cyber
- hackernews
---
### Compromission de la clé de vérification Keystone : 18 835 portefeuilles matériels mis au rebut

Keystone a été victime d'une intrusion sur son site web, permettant à un attaquant d'obtenir la clé privée utilisée pour authentifier l'authenticité de ses portefeuilles matériels. Bien que les clés privées des utilisateurs et les phrases de récupération ne soient pas compromises, cette faille permet la création de contrefaçons capables de passer avec succès le test de vérification officiel.

**Points clés :**
*   **Données exposées :** Environ 25 964 enregistrements de clients (noms, contacts, adresses de livraison) ont été dérobés. Les informations bancaires et les documents d'identité ne sont pas concernés.
*   **Risque de contrefaçon :** La clé compromise permet de produire des appareils frauduleux qui semblent légitimes aux yeux du système de vérification de l'entreprise.
*   **Réponse de l'entreprise :** 18 835 unités invendues seront détruites. Les nouveaux appareils utiliseront une clé différente.

**Vulnérabilités :**
*   **Vecteur d'attaque :** Exploitation d'une vulnérabilité par élévation de privilèges dans un outil tiers de surveillance de données utilisé sur le site web de Keystone. (Aucun identifiant CVE spécifique n'a été publié par le fabricant).
*   **Gestion des données :** Défaillance d'un outil automatisé de suppression des données clients, entraînant une rétention excédant les 180 jours promis.

**Recommandations :**
*   **Appareils reçus avant le 20 octobre :** Considérés comme sûrs s'ils passent le test de vérification.
*   **Appareils reçus après le 20 octobre :** Ne pas utiliser avant confirmation explicite de leur authenticité par le support technique de Keystone (support@keyst.one).
*   **Vigilance accrue :** Se méfier des tentatives de phishing (e-mails, appels ou SMS) proposant des remboursements ou des remplacements de produits. Keystone ne demande jamais de retourner un appareil par ces moyens.
*   **Sécurité des données :** Keystone réduit désormais la durée de conservation des données clients de 180 à 90 jours.
*   **Bonnes pratiques :** Ne jamais saisir de phrase de récupération sur un appareil non commandé et accéder directement au site officiel (`keyst.one`) plutôt que de cliquer sur des liens reçus par message.

---
[Source](https://thehackernews.com/2026/10/keystone-to-destroy-18835-hardware.html){:target="_blank"}
