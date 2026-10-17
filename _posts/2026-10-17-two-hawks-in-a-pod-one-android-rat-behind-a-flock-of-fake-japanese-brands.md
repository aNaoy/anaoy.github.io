---
title: 'Two Hawks in a Pod: one Android RAT behind a flock of fake Japanese brands'
date: 2026-10-17
permalink: /posts/2026/10/17/two-hawks-in-a-pod-one-android-rat-behind-a-flock-of-fake-japanese-brands/
tags:
- veille-cyber
- zerodaysfans
---
### Analyse de la campagne malveillante "Black Hawk" sur Android

Une campagne de cybercriminalité financière cible les utilisateurs d'Android via un RAT (Remote Access Trojan) hautement modulaire, piloté par des panneaux de contrôle sous les noms "Black Hawk" (黑鹰) et "Eagle" (雄鹰).

**Points clés de l'attaque :**
*   **Propagation :** Le malware se présente sous forme de "dropper" déguisé en applications légitimes (services fiscaux japonais, applications bancaires comme Rakuten/SMBC, ou escroqueries à l'investissement type "SpaceX 6G").
*   **Technique d'évasion :** Les noms des applications utilisent des caractères invisibles (zero-width non-joiners) pour contourner les filtres de détection basés sur les noms.
*   **Infrastructure :** Utilisation simultanée de plusieurs panneaux de contrôle de type "hawk-branded" pour piloter les appareils infectés.
*   **Mécanismes de protection :** Double méthode de packing : un stub XOR natif (`libsa.so`) ou une machine virtuelle open-source (`nmmp`) pour dissimuler le code malveillant.

**Fonctionnalités du RAT :**
*   **Espionnage :** Capture des codes de verrouillage (PIN, motifs), interception des saisies clavier et enregistrement d'écran.
*   **Fraude financière :** Extraction ciblée de données dans les applications de paiement (Alipay, WeChat).
*   **Contrôle à distance :** Utilisation des services d'accessibilité pour simuler des gestes, naviguer et effectuer des transactions à l'insu de l'utilisateur.
*   **Escalade de privilèges :** Auto-appairage via ADB sans fil (SPAKE2) pour s'accorder les permissions `WRITE_SECURE_SETTINGS`.
*   **Persistance :** Multiples récepteurs (boot, alarmes, administrateur système) garantissant une exécution continue en arrière-plan.

**Recommandations de sécurité :**
*   **Détection comportementale :** Surveiller la présence du service `PlatformAssistDaemon` et des bibliothèques `libspake2.so` / `libdxs.so` dans des applications tierces.
*   **Analyse du dropper :** Ne pas se fier au certificat de signature (utilisant souvent `CN=Android`). Rechercher les composants spécifiques du dropper : activités `Wv`, `Bv` et récepteur `Ir` associé à l'action `INSTALL_COMPLETE`.
*   **Indicateurs d'installation :** Bloquer les applications demandant de manière suspecte la permission `REQUEST_INSTALL_PACKAGES`.
*   **Bonnes pratiques :** Ne jamais installer d'applications en dehors des stores officiels et rester vigilant face aux sites web invitant au téléchargement direct d'APK, même s'ils imitent des sites de confiance (ex: e-Tax).

---
[Source](https://starlabs.sg/blog/2026/10-two-hawks-in-a-pod-one-android-rat-behind-a-flock-of-fake-japanese-brands/){:target="_blank"}
