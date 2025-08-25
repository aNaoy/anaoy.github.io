---
title: 'Malicious Android apps with 19M installs removed from Google Play'
date: 2025-08-25
permalink: /posts/2025/08/25/malicious-android-apps-with-19m-installs-removed-from-google-play/
tags:
- veille-cyber
- bleepingcomp
---
**Vague de Malware sur Google Play : 77 Applications Malveillantes Supprimées**

Plus de 77 applications Android malveillantes, totalisant plus de 19 millions d'installations, ont été identifiées et supprimées de Google Play. Ces applications distribuaient diverses familles de malwares, dont Adware (majoritaire), Joker, Harly et des chevaux de Troie bancaires comme Anatsa. Le malware Joker, présent dans près de 25% des applications analysées, est capable d'exfiltrer des données sensibles et de souscrire les utilisateurs à des services premium. Le cheval de Troie bancaire Anatsa a particulièrement évolué, élargissant sa cible à 831 applications bancaires et de cryptomonnaies, utilisant des techniques d'évasion avancées et abusant des permissions d'accessibilité pour voler des identifiants et des informations bancaires.

**Points Clés :**

*   **Volume d'Installations :** Plus de 19 millions d'installations cumulées pour les applications malveillantes.
*   **Familles de Malwares :** Prédominance d'Adware, suivi de Joker, Harly, et Anatsa.
*   **Ciblage :** Anatsa cible désormais 831 applications bancaires et de cryptomonnaies.
*   **Techniques d'Évasion :** Utilisation d'archives APK malformées, déchiffrement de chaînes basé sur DES, détection d'émulation, et changements périodiques de noms de packages et de hachages.
*   **Types d'Applications Leurre :** Outils, applications de personnalisation, divertissement, photographie et design sont les catégories les plus utilisées.

**Vulnérabilités et Comportements Malveillants :**

*   **Joker :** Lecture et envoi de SMS, prise de captures d'écran, appels téléphoniques, vol de listes de contacts, accès aux informations de l'appareil, souscription à des services premium.
*   **Maskware :** Se fait passer pour des applications légitimes tout en volant des identifiants, des informations bancaires, des données de localisation et des SMS en arrière-plan. Peut également servir de chargeur pour d'autres malwares.
*   **Harly :** Variante de Joker, se cache dans des applications populaires (jeux, fonds d'écran, lampes de poche, éditeurs de photos) avec une charge utile malveillante dissimulée.
*   **Anatsa :**
    *   Abuse des permissions d'accessibilité pour obtenir des privilèges étendus.
    *   Récupère des pages de phishing pour plus de 831 applications.
    *   Ajout d'un module enregistreur de frappe (keylogger) pour le vol de données générique.
    *   Utilisation d'une application nommée 'Document Reader – File Manager' comme leurre, téléchargeant la charge utile Anatsa après installation pour échapper à la revue de code.

**Recommandations :**

*   Maintenir le service Play Protect de Google activé sur les appareils Android pour signaler les applications malveillantes.
*   En cas d'infection par Anatsa, contacter la banque pour protéger les comptes et les identifiants potentiellement compromis.
*   Pour minimiser les risques, ne faire confiance qu'à des éditeurs réputés.
*   Lire attentivement les avis des utilisateurs avant d'installer une application.
*   Accorder uniquement les permissions strictement nécessaires à la fonctionnalité principale de l'application.

---
[Source](https://www.bleepingcomputer.com/news/security/malicious-android-apps-with-19m-installs-removed-from-google-play/){:target="_blank"}
