---
title: 'Unpatched Firmware Flaw Exposes TOTOLINK EX200 to Full Remote Device Takeover'
date: 2026-01-06
permalink: /posts/2026/01/06/unpatched-firmware-flaw-exposes-totolink-ex200-to-full-remote-device-takeover/
tags:
- veille-cyber
- hackernews
---
**Faille critique du firmware TOTOLINK EX200 : Prise de contrôle à distance**

Une vulnérabilité du firmware du répéteur Wi-Fi TOTOLINK EX200 permet à un attaquant authentifié de prendre le contrôle total de l'appareil. Cette faille, identifiée sous la référence **CVE-2025-65606**, découle d'une mauvaise gestion des erreurs lors du téléversement du firmware.

**Points Clés :**

*   **Nature de la faille :** Mauvaise gestion des erreurs dans la logique de téléversement du firmware.
*   **Impact :** Permet à un attaquant déjà authentifié sur l'interface web de déclencher l'activation d'un service Telnet non authentifié avec des privilèges root.
*   **Conséquences :** Prise de contrôle complète du système, permettant la manipulation de la configuration, l'exécution de commandes arbitraires et l'établissement de persistance sur l'appareil.
*   **Exploitation :** Nécessite une authentification préalable sur l'interface de gestion web de l'appareil.
*   **Statut du correctif :** TOTOLINK n'a pas publié de correctif. Le produit ne semble plus être activement maintenu, le dernier aggiornamento du firmware datant de février 2023.

**Vulnérabilités :**

*   **CVE-2025-65606**

**Recommandations :**

*   Restreindre l'accès administratif aux réseaux de confiance.
*   Empêcher les utilisateurs non autorisés d'accéder à l'interface de gestion.
*   Surveiller les activités anormales sur l'appareil.
*   Envisager la mise à niveau vers un modèle pris en charge et activement maintenu.

---
[Source](https://thehackernews.com/2026/01/unpatched-firmware-flaw-exposes.html){:target="_blank"}
