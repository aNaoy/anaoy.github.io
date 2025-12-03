---
title: 'Brazil Hit by Banking Trojan Spread via WhatsApp Worm and RelayNFC NFC Relay Fraud'
date: 2025-12-03
permalink: /posts/2025/12/03/brazil-hit-by-banking-trojan-spread-via-whatsapp-worm-and-relaynfc-nfc-relay-fraud/
tags:
- veille-cyber
- hackernews
---
### Menace Bancaire Multi-facettes au Brésil

Une campagne de cybersécurité sophistiquée cible les utilisateurs brésiliens, combinant un cheval de Troie bancaire diffusé via un ver sur WhatsApp et une nouvelle souche de malware Android exploitant les technologies NFC.

**Points Clés :**

*   **Water Saci** : Ce groupe de menace utilise une chaîne d'infection complexe impliquant des fichiers HTA et PDF pour propager un cheval de Troie bancaire sur WhatsApp Web. La transition vers un script Python, potentiellement assistée par IA, rend la propagation plus rapide et résiliente.
*   **Ciblage Spécifique** : Le malware vérifie la langue du système (portugais brésilien) et recherche des applications bancaires brésiliennes connues (Bradesco, Itaú, etc.). Il surveille également l'historique de navigation pour identifier les visites sur des sites bancaires spécifiques.
*   **Mécanismes d'Infection** : Les utilisateurs sont trompés par des messages provenant de contacts connus, les incitant à ouvrir des pièces jointes malveillantes. Les fichiers HTA exécutent des scripts qui téléchargent le malware, tandis que les PDF invitent à des mises à jour frauduleuses.
*   **RelayNFC** : Un nouveau malware Android, construit avec React Native et Hermes bytecode, permet des attaques par relais NFC. Il vise à voler des données de paiement sans contact pour effectuer des transactions frauduleuses.
*   **Ingénierie Sociale** : RelayNFC est distribué via des sites de phishing qui incitent les utilisateurs à installer le malware pour "sécuriser" leurs cartes de paiement.

**Vulnérabilités et Exploitations :**

*   Aucune CVE spécifique n'est mentionnée dans l'article pour les vulnérabilités exploitées.
*   Exploitation de la confiance des utilisateurs sur WhatsApp et via des techniques de phishing.
*   Utilisation de fichiers HTA et PDF pour déclencher des scripts malveillants.
*   Exploitation de la technologie NFC pour le transfert et la capture de données de paiement.
*   Évitement des analyses grâce à des techniques anti-virtualisation et à l'utilisation de React Native/Hermes bytecode.

**Recommandations :**

*   **Prudence avec les messages et pièces jointes** : Ne pas ouvrir de pièces jointes ou cliquer sur des liens provenant de sources inconnues ou suspectes, même si elles proviennent de contacts connus (qui peuvent avoir été compromis).
*   **Mises à jour logicielles** : Maintenir à jour le système d'exploitation, les navigateurs et les applications de sécurité.
*   **Vigilance sur les applications mobiles** : Être prudent lors de l'installation d'applications, surtout celles demandant des permissions sensibles comme l'accès au NFC ou aux SMS.
*   **Surveillance des transactions** : Vérifier attentivement les relevés bancaires et de cartes de crédit pour toute activité suspecte.
*   **Renforcement de la sécurité des appareils** : Utiliser des mots de passe forts et des méthodes d'authentification à deux facteurs.
*   **Sensibilisation** : Se tenir informé des nouvelles menaces et des tactiques utilisées par les cybercriminels.

---
[Source](https://thehackernews.com/2025/12/brazil-hit-by-banking-trojan-spread-via.html){:target="_blank"}
