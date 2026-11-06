---
title: 'Groklem: an Android banker that rents Grok to read your texts'
date: 2026-11-06
permalink: /posts/2026/11/06/groklem-an-android-banker-that-rents-grok-to-read-your-texts/
tags:
- veille-cyber
- zerodaysfans
---
### Analyse du Trojan Bancaire « Groklem »

Groklem est un cheval de Troie bancaire Android sophistiqué qui délègue l'analyse des données volées à une intelligence artificielle (xAI Grok). Le malware agit comme un intermédiaire : il subtilise les SMS et l'inventaire des applications, les transmet à Grok pour en extraire des informations financières (soldes, codes OTP, alertes bancaires), puis renvoie une synthèse structurée à l'attaquant.

#### Points clés
*   **Fonctionnement par IA :** Contrairement aux malwares classiques utilisant des règles fixes, Groklem envoie les messages du téléphone à l'API de xAI (`grok-4.20-0309-non-reasoning`) pour interpréter intelligemment le contenu.
*   **Pilotage à distance :** La clé d'API xAI n'est pas intégrée au code ; elle est fournie dynamiquement par l'attaquant via son canal de commande (C2), liant chaque campagne à un compte utilisateur spécifique.
*   **Escalade de privilèges (ADB) :** Le malware utilise la bibliothèque *Kadb* pour s'appairer localement avec le démon ADB du téléphone (via le débogage sans fil). Cela lui permet de s'octroyer silencieusement des droits d'accessibilité et d'accéder à des privilèges système.
*   **Persistance et invisibilité :** Le malware empêche l'utilisateur de désinstaller l'application ou de révoquer ses droits d'accessibilité en détectant les écrans de configuration système et en forçant le retour à l'écran d'accueil.
*   **Ciblage :** Bien que non limité géographiquement, le malware montre une préférence marquée pour l'Inde et le Bangladesh (lures basés sur *eChallan*, hooks pour *PhonePe* et *bKash*).

#### Vulnérabilités exploitées
*   **Abus de l'Accessibilité Android :** Utilisation des services d'accessibilité pour intercepter les saisies au clavier (keylogging), capturer des données dans des applications tierces via des overlays, et automatiser des actions.
*   **Détournement d'ADB :** Exploitation du débogage sans fil pour élever ses privilèges au niveau `shell` (uid 2000) et contourner les protections natives d'Android.
*   **WebViews non sécurisées :** Injection de JavaScript pour capturer en temps réel les identifiants, codes PIN et OTP saisis dans des formulaires web.

#### Recommandations de sécurité
1.  **Désactivation du débogage sans fil :** Vérifiez régulièrement que l'option "Débogage sans fil" est désactivée dans les options pour les développeurs.
2.  **Gestion stricte des services d'accessibilité :** N'accordez jamais de droits d'accessibilité à des applications provenant de sources non fiables ou suspectes.
3.  **Surveillance des permissions :** Examinez les applications ayant des droits de "dessin sur d'autres applications" (Overlay) et de lecture des SMS.
4.  **Authentification multifacteur (MFA) :** Utilisez des méthodes MFA basées sur des applications d'authentification ou des clés physiques plutôt que les codes SMS (OTPs), car ces derniers sont la cible principale de Groklem.
5.  **Détection réseau :** Bloquer les communications vers les domaines connus de xAI (`api.x.ai`) si l'activité est jugée suspecte, et surveiller les connexions sortantes vers des ports inhabituels (9999, 8888, 5059).

---
[Source](https://starlabs.sg/blog/2026/11-groklem-an-android-banker-that-rents-grok-to-read-your-texts/){:target="_blank"}
