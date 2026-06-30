---
title: 'AirDrop and Quick Share Flaws Let Nearby Attackers Trigger Crashes and Bypass Checks'
date: 2026-06-30
permalink: /posts/2026/06/30/airdrop-and-quick-share-flaws-let-nearby-attackers-trigger-crashes-and-bypass-checks/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités sans fil : AirDrop et Quick Share sous surveillance

Des chercheurs du CISPA ont identifié six failles de sécurité critiques au sein des protocoles de partage sans fil **AirDrop** (Apple) et **Quick Share** (Android/Windows). Ces vulnérabilités permettent à un attaquant situé à proximité (10 à 30 mètres) de provoquer des plantages systèmes ou de contourner des mécanismes de contrôle de session sans interaction préalable avec l'utilisateur.

**Points clés :**
*   **Impact global :** Ces failles touchent des écosystèmes comptant plus de 5 milliards d'appareils.
*   **AirDrop (Apple) :** Trois vulnérabilités affectent le service `sharingd`. L'envoi répété de requêtes malformées peut paralyser le partage de fichiers, mais aussi d'autres services comme AirPlay, Handoff ou NameDrop. Une faille de type *stack overflow* dans l'analyseur XML de Foundation expose potentiellement plusieurs systèmes (macOS, iOS, watchOS, etc.).
*   **Quick Share (Samsung/Google) :** Des failles permettent de contourner la poignée de main cryptographique, forçant des connexions non autorisées ou interceptant des messages de contrôle.
*   **Quick Share pour Windows :** Une vulnérabilité de type *use-after-free* a été découverte, potentiellement exploitable pour l'exécution de code arbitraire, car la protection *Control Flow Guard* est désactivée dans l'application.

**Vulnérabilités identifiées :**
*   CVE en attente pour la majorité des failles (Apple, Google et Samsung).
*   *Note :* Bien que la plupart des CVE soient en attente, le risque de récurrence sur le logiciel Quick Share pour Windows est souligné, rappelant les précédentes CVE-2024-38271, CVE-2024-38272 et CVE-2024-10668.

**Recommandations :**
*   **Mises à jour :** Installer immédiatement les dernières versions des systèmes d'exploitation (iOS/macOS 26.5.2+) et mettre à jour l'application Quick Share pour Windows.
*   **Configuration de visibilité :** Désactiver le paramètre "Tout le monde" (*Everyone*) pour AirDrop et Quick Share. Privilégier le mode "Contacts uniquement" ou désactiver ces services lorsqu'ils ne sont pas activement utilisés.
*   **Prudence :** Être vigilant dans les lieux publics fréquentés (aéroports, gares, conférences), zones où la portée du signal Bluetooth/Wi-Fi des attaquants est la plus efficace.

---
[Source](https://thehackernews.com/2026/06/airdrop-and-quick-share-flaws-let.html){:target="_blank"}
