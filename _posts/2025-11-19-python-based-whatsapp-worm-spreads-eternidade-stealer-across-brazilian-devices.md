---
title: 'Python-Based WhatsApp Worm Spreads Eternidade Stealer Across Brazilian Devices'
date: 2025-11-19
permalink: /posts/2025/11/19/python-based-whatsapp-worm-spreads-eternidade-stealer-across-brazilian-devices/
tags:
- veille-cyber
- hackernews
---
## Campagne de Maliciel Bancaire via WhatsApp au Brésil

Une campagne de cybercriminalité cible les utilisateurs brésiliens en utilisant un maliciel bancaire appelé **Eternidade Stealer**. La distribution s'effectue via un ver informatiques se propageant sur WhatsApp, désormais basé sur un script Python remplaçant les scripts PowerShell précédents. Le maliciel exploite le protocole IMAP pour récupérer dynamiquement les adresses des serveurs de commande et de contrôle (C2), permettant aux attaquants de mettre à jour leur infrastructure.

Cette campagne s'inscrit dans une tendance plus large d'utilisation de WhatsApp comme vecteur de propagation au Brésil, et s'appuie sur des maliciels bancaires développés en Delphi, un langage populaire dans la région.

### Points Clés :

*   **Vecteur d'infection initial** : Un script Visual Basic Script (VBS) obfusqué, écrit principalement en portugais.
*   **Mécanisme de propagation** : Un script Python utilise la bibliothèque WPPConnect pour automatiser l'envoi de messages malveillants sur WhatsApp à partir de comptes compromis. Il collecte la liste de contacts de la victime et envoie un message avec une pièce jointe malveillante.
*   **Composant d'infection secondaire** : Un installateur MSI dépose un script AutoIt qui lance le vol d'informations.
*   **Ciblage géographique** : Le maliciel vérifie la langue du système d'exploitation pour s'assurer qu'il est configuré en portugais brésilien, indiquant un ciblage spécifique du Brésil.
*   **Vol d'informations** : Eternidade Stealer recherche activement les informations d'identification des services bancaires, des plateformes de paiement et des portefeuilles de cryptomonnaies (ex: Bradesco, BTG Pactual, Binance, MetaMask).
*   **Technique d'injection** : Le maliciel utilise la technique de "process hollowing" pour injecter sa charge utile dans le processus légitime "svchost.exe".
*   **Infrastructure de commande et contrôle (C2)** : Les adresses C2 sont récupérées via une boîte aux lettres d'email terra.com[.]br, permettant une mise à jour dynamique. Un système de redirection surveille les tentatives de connexion.
*   **Capacités du maliciel** : Enregistrement des frappes au clavier, capture d'écran, vol de fichiers, et exécution de commandes à distance.

### Vulnérabilités :

L'article ne mentionne pas de CVE spécifiques associées directement à ce maliciel ou à sa méthode de propagation. L'exploitation repose principalement sur :

*   **Ingénierie sociale** : Convaincre les utilisateurs de télécharger et d'exécuter des pièces jointes malveillantes.
*   **Exploitation de la confiance dans WhatsApp** : Utiliser l'application de messagerie pour se faire passer pour un contact légitime.
*   **Automatisation via API** : L'utilisation de bibliothèques comme WPPConnect pour l'automatisation des actions sur WhatsApp.

### Recommandations :

*   **Vigilance accrue** : Être particulièrement attentif aux messages suspects reçus sur WhatsApp, même s'ils proviennent de contacts connus.
*   **Méfiance envers les pièces jointes** : Ne pas ouvrir les pièces jointes inattendues, en particulier celles avec des extensions exécutables (comme .msi) ou des scripts.
*   **Sécurité des systèmes** : Maintenir les systèmes d'exploitation et les logiciels de sécurité à jour.
*   **Sensibilisation** : Informer les utilisateurs des risques liés aux campagnes de phishing et de maliciels diffusés via les réseaux sociaux et les applications de messagerie.
*   **Surveillance du réseau** : Les équipes de sécurité doivent rester vigilantes face aux indicateurs de compromission liés à cette campagne, tels que les exécutions de scripts MSI ou Python inhabituelles, et les communications avec des serveurs C2 suspects.

---
[Source](https://thehackernews.com/2025/11/python-based-whatsapp-worm-spreads.html){:target="_blank"}
