---
title: 'Intellexa Leaks Reveal Zero-Days and Ads-Based Vector for Predator Spyware Delivery'
date: 2025-12-05
permalink: /posts/2025/12/05/intellexa-leaks-reveal-zero-days-and-ads-based-vector-for-predator-spyware-delivery/
tags:
- veille-cyber
- hackernews
---
**Exposition des Capacités Avancées du Logiciel Espion Predator**

Une enquête conjointe, basée sur des documents divulgués par Intellexa, met en lumière les méthodes sophistiquées utilisées par leur logiciel espion Predator pour cibler des individus. Une récente attaque a ciblé un avocat pakistanais, illustrant l'utilisation de liens malveillants via des plateformes de messagerie. Le logiciel espion, également connu sous d'autres noms tels que Helios et Nova, est conçu pour extraire discrètement des données sensibles des appareils Android et iOS.

**Points Clés :**

*   **Méthodes de Diffusion :** Predator utilise des techniques d'exploitation de vulnérabilités "zero-click" ou "one-click" via des liens envoyés par messagerie (WhatsApp, par exemple). Des vecteurs d'attaque plus sophistiqués, comme les systèmes d'injection réseau (Mars et Jupiter) exploitant des failles dans la navigation web, et l'écosystème publicitaire (Aladdin) ciblant les utilisateurs via des publicités malveillantes, sont également documentés.
*   **Exploitation de Vulnérabilités Zero-Day :** Intellexa a exploité plusieurs vulnérabilités zero-day critiques dans Android, Google Chrome et Apple Safari.
*   **Collecte de Données Étendue :** Une fois installé, Predator peut accéder aux applications de messagerie, aux appels, aux e-mails, à la localisation, aux captures d'écran, aux mots de passe, et même activer le microphone et la caméra de l'appareil.
*   **Accès à Distance des Opérateurs :** Des preuves suggèrent qu'Intellexa pourrait avoir la capacité d'accéder à distance aux systèmes de surveillance de ses clients, soulevant des questions sur la responsabilité en cas d'abus.
*   **Expansion Géographique :** L'activité liée à Predator a été détectée dans plus d'une douzaine de pays, principalement en Afrique, indiquant une demande croissante.

**Vulnérabilités (avec CVE) :**

*   **Android Runtime :** CVE-2025-48543 (Use-after-free)
*   **Google Chrome (V8) :** CVE-2025-6554, CVE-2023-4762, CVE-2023-3079, CVE-2023-2033, CVE-2021-38003, CVE-2021-38000, CVE-2021-37976, CVE-2021-37973 (Type confusion, Use-after-free, Information leak, Inappropriate implementation, Insufficient validation)
*   **Google Chrome (Skia) :** CVE-2023-2136 (Integer overflow)
*   **Apple Safari :** CVE-2023-41993 (WebKit JIT RCE)
*   **Apple (Kernel IPC) :** CVE-2023-41992 (Use-After-Free)
*   **Apple (Security framework) :** CVE-2023-41991 (Certificate validation bypass)
*   **Arm (GPU Kernel Driver) :** CVE-2024-4610 (Use-after-free)
*   **Android Kernel :** CVE-2021-1048 (Use-After-Free)

**Recommandations :**

Bien que l'article ne formule pas directement de recommandations pour les utilisateurs finaux, il met en évidence la nécessité d'une vigilance accrue face aux liens suspects provenant de sources inconnues. L'existence de vulnérabilités zero-day exploitées souligne l'importance des mises à jour logicielles régulières pour les systèmes d'exploitation et les navigateurs afin de corriger ces failles dès leur découverte. L'utilisation de vecteurs d'attaque publicitaires indique également un risque accru lors de la navigation sur des sites web affichant des publicités.

---
[Source](https://thehackernews.com/2025/12/intellexa-leaks-reveal-zero-days-and.html){:target="_blank"}
