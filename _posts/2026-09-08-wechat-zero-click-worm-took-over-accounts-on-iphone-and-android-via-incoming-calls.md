---
title: 'WeChat Zero-Click Worm Took Over Accounts on iPhone and Android via Incoming Calls'
date: 2026-09-08
permalink: /posts/2026/09/08/wechat-zero-click-worm-took-over-accounts-on-iphone-and-android-via-incoming-calls/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique "Zero-Click" dans WeChat : une faille par appel entrant

Des chercheurs en cybersécurité de la firme Calif ont démontré l'existence d'un ver informatique capable de compromettre intégralement un compte WeChat via un simple appel entrant. Cette attaque, qualifiée de "zero-click", permet à un attaquant de prendre le contrôle total du compte sans aucune interaction de la part de la victime (pas besoin de décrocher).

**Points clés :**
*   **Mécanisme :** L'attaquant doit figurer dans la liste de contacts de la victime. Une fois le compte compromis, le ver peut se propager automatiquement aux autres contacts de la cible.
*   **Impact :** L'attaquant obtient un accès complet au compte (lecture/envoi de messages, appels, gestion des paiements et mini-programmes). L'appareil lui-même reste sous le contrôle de son propriétaire, mais l'identité numérique est usurpée.
*   **Démonstration :** L'attaque a été validée avec succès sur des appareils Android et iOS.
*   **Contexte :** La vulnérabilité a été découverte grâce à l'assistance d'une intelligence artificielle. Tencent a été informé en juillet 2026.

**Vulnérabilités :**
*   **CVE :** Aucune CVE n'a été attribuée à ce jour.
*   **Versions concernées :** WeChat 8.0.75 (iOS) et 8.0.76 (Android) et versions antérieures. Aucune liste officielle exhaustive n'a été publiée.

**Recommandations :**
*   **Mise à jour :** Assurez-vous d'utiliser la version la plus récente de l'application WeChat (au minimum la version 8.0.77 sur Android et 8.0.76 sur iOS, publiées le 21 août 2026).
*   **Correction côté serveur :** Tencent a déployé un correctif global côté serveur dès fin août ; il est donc crucial de maintenir l'application à jour pour garantir la compatibilité avec ces sécurités.
*   **Prudence :** Bien que l'exploit soit bloqué, la meilleure protection contre les attaques de type "social engineering" reste la restriction de sa liste de contacts aux personnes de confiance, afin de limiter la surface d'attaque en cas de découverte de nouvelles vulnérabilités similaires.

---
[Source](https://thehackernews.com/2026/09/wechat-zero-click-worm-took-over.html){:target="_blank"}
