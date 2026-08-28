---
title: 'Android 17 Adds OS-Wide ECH to Hide Website Visits From Network Providers'
date: 2026-08-28
permalink: /posts/2026/08/28/android-17-adds-os-wide-ech-to-hide-website-visits-from-network-providers/
tags:
- veille-cyber
- hackernews
---
### Renforcement de la confidentialité et de la sécurité réseau dans Android 17

Android 17 introduit des protections réseau natives majeures pour améliorer la confidentialité des utilisateurs et réduire l'exposition aux attaques cellulaires.

**Points clés :**
*   **Encrypted Client Hello (ECH) :** Intégration au niveau du système d'exploitation pour masquer les noms de domaine visités aux fournisseurs d'accès.
*   **ECH GREASE :** Activation par défaut pour uniformiser les connexions et éviter le profilage des utilisateurs, même sur les serveurs ne supportant pas l'ECH.
*   **Protection du réseau local :** Exigence de permission explicite pour les applications souhaitant scanner ou se connecter à d'autres appareils locaux.
*   **Certificate Transparency (CT) :** Activation par défaut pour garantir que tous les sites web sont enregistrés dans un registre public, renforçant l'intégrité des certificats TLS.
*   **Désactivation du réseau 2G :** Les opérateurs peuvent désormais désactiver nativement le support 2G pour éviter les attaques par rétrogradation (*downgrade attacks*) et les stations de base frauduleuses.

**Vulnérabilités adressées :**
*   **Attaques par rétrogradation (2G) :** Risque d'interception de trafic et réception de messages malveillants via des fausses antennes (SMS blasters). Aucune CVE spécifique n'est citée, mais il s'agit d'une correction structurelle contre une surface d'attaque historique.
*   **Profilage réseau :** Fuite de métadonnées DNS permettant de tracer les habitudes de navigation.

**Recommandations :**
*   **Pour les développeurs :** Utiliser la bibliothèque **OkHttp**, qui intègre désormais le support ECH, pour permettre aux applications tierces de bénéficier de cette protection.
*   **Pour les administrateurs et utilisateurs :** Vérifier la disponibilité de l'option de désactivation du 2G auprès de son opérateur mobile pour limiter les vecteurs d'attaques cellulaires.

---
[Source](https://thehackernews.com/2026/08/android-17-adds-os-wide-ech-to-hide.html){:target="_blank"}
