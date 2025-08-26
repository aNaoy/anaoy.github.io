---
title: 'HOOK Android Trojan Adds Ransomware Overlays, Expands to 107 Remote Commands'
date: 2025-08-26
permalink: /posts/2025/08/26/hook-android-trojan-adds-ransomware-overlays-expands-to-107-remote-commands/
tags:
- veille-cyber
- hackernews
---
**Le cheval de Troie bancaire HOOK sur Android intègre des fonctionnalités de ransomware et étend ses commandes**

Une nouvelle version du logiciel malveillant bancaire Android HOOK a été découverte, se distinguant par sa capacité à afficher des écrans de rançongiciel en plein écran pour extorquer des victimes. L'écran, affichant un message d'alerte "*WARNING*", une adresse de portefeuille et un montant, est déclenché à distance par le serveur de commande et contrôle (C2) via la commande "ransome" et peut être retiré avec "delete_ransome".

Ce cheval de Troie, potentiellement dérivé du logiciel malveillant ERMAC dont le code source a fuité, cible les applications financières en utilisant des écrans de simulation pour voler les identifiants. Il abuse également des services d'accessibilité Android pour automatiser des fraudes et prendre le contrôle à distance des appareils. Ses fonctionnalités incluent l'envoi de SMS, le streaming d'écran, la capture de photos par la caméra frontale et le vol de cookies et de phrases de récupération de portefeuilles de cryptomonnaies.

La dernière itération de HOOK supporte désormais 107 commandes à distance, dont 38 nouvelles. Parmi celles-ci figurent des commandes pour afficher des superpositions transparentes afin de capturer des gestes d'utilisateur ("start_record_gesture"), des superpositions NFC factices pour obtenir des données sensibles ("takenfc"), des fausses interfaces de paiement pour collecter des informations de carte bancaire ("takencard"), et des invites trompeuses pour dérober les codes PIN ou schémas de verrouillage de l'appareil ("unlock_pin").

HOOK est diffusé à grande échelle via des sites de phishing et de faux dépôts GitHub, une méthode également utilisée par d'autres familles de logiciels malveillants Android comme ERMAC et Brokewell. L'évolution de HOOK montre une convergence croissante des chevaux de Troie bancaires avec les tactiques de logiciels espions et de rançongiciels, augmentant ainsi le risque pour les institutions financières, les entreprises et les utilisateurs finaux.

**Points clés:**

*   La dernière version du cheval de Troie bancaire Android HOOK inclut une fonctionnalité de rançongiciel avec des écrans de simulation.
*   Le malware peut voler des identifiants, automatiser des fraudes via les services d'accessibilité, et contrôler des appareils à distance.
*   Il peut également voler des informations sensibles relatives aux portefeuilles de cryptomonnaies.
*   HOOK supporte désormais 107 commandes à distance, incluant de nouvelles actions pour les superpositions et la capture d'informations sensibles.
*   La diffusion se fait par le biais de sites de phishing et de dépôts GitHub.

**Vulnérabilités/Fonctionnalités exploitées:**

*   Services d'accessibilité Android pour l'automatisation des fraudes et l'obtention de permissions supplémentaires.
*   Superpositions d'écran pour simuler des interfaces légitimes (applications bancaires, Google Pay, paiement NFC) afin de voler des données sensibles.
*   Écrans de simulation pour capturer les gestes de l'utilisateur et les codes de déverrouillage de l'appareil.

**Recommandations:**

*   Faire preuve de prudence lors du téléchargement d'applications, en privilégiant les sources officielles.
*   Être vigilant face aux sites de phishing et aux fausses plateformes de distribution d'applications.
*   Vérifier attentivement les permissions demandées par les applications et les désactiver si elles ne sont pas nécessaires.
*   Maintenir les systèmes d'exploitation Android et les applications à jour pour bénéficier des derniers correctifs de sécurité.

---
[Source](https://thehackernews.com/2025/08/hook-android-trojan-adds-ransomware.html){:target="_blank"}
