---
title: 'Unpatched Shark Vacuum Flaw Could Let Attackers Control Other Vacuums Region-Wide'
date: 2026-07-16
permalink: /posts/2026/07/16/unpatched-shark-vacuum-flaw-could-let-attackers-control-other-vacuums-region-wide/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité majeure sur les aspirateurs connectés Shark

Des chercheurs ont identifié une faille critique dans la gestion des certificats AWS IoT des aspirateurs Shark, permettant à un attaquant de prendre le contrôle total d'appareils à l'échelle d'une région AWS entière. En extrayant les certificats d'un appareil, un tiers peut envoyer des commandes arbitraires (via `Exec_Command`) à d'autres aspirateurs, accédant ainsi aux flux vidéo, aux cartes des domiciles et aux données Wi-Fi.

**Points clés :**
*   **Cause racine :** Utilisation de politiques AWS IoT trop permissives qui ne restreignent pas les communications au seul appareil concerné.
*   **Méthode :** Accès physique via les ports UART pour récupérer les certificats. Les commandes sont ensuite injectées via le "device shadow" d'AWS.
*   **Portée :** Des centaines de milliers d'appareils potentiellement vulnérables ont été observés.
*   **Divulgation :** La faille a été signalée au fabricant en mars 2024, mais aucune correction n'a été déployée, malgré une politique de divulgation responsable.

**Vulnérabilités :**
*   **CVE :** Aucune assignée à ce jour.
*   **Référence AWS :** `IOT_POLICY_OVERLY_PERMISSIVE_CHECK` (La politique autorise `publish`/`subscribe` sur `aws/things/*` au lieu d'utiliser `${iot:Connection.Thing.ThingName}`).

**Recommandations :**
*   **Utilisateurs :** La seule mesure de protection efficace actuelle consiste à déconnecter l'aspirateur du réseau Wi-Fi, ce qui empêche toute commande à distance.
*   **Fabricant :** Appliquer une correction côté serveur (AWS) pour restreindre les politiques d'accès et, idéalement, réémettre des certificats correctement sécurisés. Aucune mise à jour de firmware n'est nécessaire pour corriger cette faille spécifique.

---
[Source](https://thehackernews.com/2026/07/unpatched-shark-vacuum-flaw-could-let.html){:target="_blank"}
