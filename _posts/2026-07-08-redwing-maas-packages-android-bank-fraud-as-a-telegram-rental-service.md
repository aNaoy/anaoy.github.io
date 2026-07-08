---
title: 'RedWing MaaS Packages Android Bank Fraud as a Telegram Rental Service'
date: 2026-07-08
permalink: /posts/2026/07/08/redwing-maas-packages-android-bank-fraud-as-a-telegram-rental-service/
tags:
- veille-cyber
- hackernews
---
### RedWing : La menace Android sous forme de service (MaaS)

RedWing est une nouvelle plateforme de « Malware-as-a-Service » (MaaS) proposée à la location sur Telegram. Ce kit permet à des cybercriminels, même novices, de déployer des applications malveillantes capables de prendre le contrôle total d'un appareil Android pour dérober des identifiants bancaires et intercepter des codes de validation (2FA).

**Points clés :**
*   **Modèle économique :** Vendu par abonnement avec support technique et guides, incluant un bot Telegram pour générer des applications personnalisées à la demande.
*   **Propagation :** Utilisation de liens de phishing redirigeant vers de fausses boutiques d'applications (imitant Google Play, Galaxy Store, etc.).
*   **Ciblage :** Le malware vise principalement des institutions financières (82 identifiées, avec une forte concentration sur le marché russe) et peut être mis à jour à distance par les attaquants.
*   **Techniques de fraude :** RedWing privilégie la fraude « sur l'appareil », opérant directement au sein des sessions bancaires légitimes des victimes.

**Vulnérabilités exploitées :**
*   **Absence de CVE spécifique :** RedWing ne repose pas sur une faille logicielle (exploit), mais sur l'ingénierie sociale. Il abuse des fonctionnalités légitimes du système Android :
    *   **Services d'accessibilité :** Utilisés pour lire l'écran, capturer des frappes clavier (keylogger) et contrôler l'interface à distance.
    *   **Gestion des SMS :** Paramétrage de l'application malveillante comme gestionnaire SMS par défaut pour intercepter les codes de sécurité.
    *   **Renvoi d'appel (MMI codes) :** Utilisation de codes comme `*21*` pour détourner les appels téléphoniques de vérification bancaire.

**Recommandations :**
*   **Pour les utilisateurs :**
    *   N'installer que des applications provenant des boutiques officielles (Google Play Store).
    *   Refuser systématiquement les demandes d'autorisation suspectes liées aux « Services d'accessibilité », à la gestion des SMS ou à l'exemption de la gestion de batterie.
    *   Se méfier des mises à jour d'applications proposées via des liens externes ou des SMS.
*   **Pour les entreprises :**
    *   Bloquer le « sideloading » (installation d'applications hors sources officielles) sur les appareils gérés.
    *   Déployer des politiques de gestion des appareils mobiles (MDM) pour restreindre l'utilisation des services d'accessibilité et les privilèges d'administration.
    *   Prioriser la détection comportementale plutôt que la recherche de noms d'applications spécifiques, ces dernières étant facilement modifiables par les attaquants.

---
[Source](https://thehackernews.com/2026/07/redwing-maas-packages-android-bank.html){:target="_blank"}
