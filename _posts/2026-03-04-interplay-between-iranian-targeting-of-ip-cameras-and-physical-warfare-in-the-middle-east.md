---
title: 'Interplay between Iranian Targeting of IP Cameras and Physical Warfare in the Middle East'
date: 2026-03-04
permalink: /posts/2026/03/04/interplay-between-iranian-targeting-of-ip-cameras-and-physical-warfare-in-the-middle-east/
tags:
- veille-cyber
- zerodaysfans
---
### Surveillance Caméra Piratée : Indicateur d'Attaques Physiques

Des groupes liés à l'Iran intensifient depuis le 28 février leurs cyberattaques contre des caméras IP de marques Hikvision et Dahua. Ces attaques, qui ont également eu lieu en janvier, ciblent des pays tels qu'Israël, le Qatar, Bahreïn, le Koweït, les Émirats Arabes Unis, Chypre et le Liban. Ces mêmes régions ont connu une activité de missiles notable attribuée à l'Iran.

Ces actions suggèrent une utilisation des caméras compromises pour l'assistance opérationnelle et l'évaluation des dommages de combat (BDA) lors d'opérations de missiles, potentiellement avant leur lancement. Le piratage de caméras pourrait donc servir de signal précurseur d'actions militaires imminentes.

**Points Clés :**

*   Augmentation significative du ciblage de caméras IP depuis le 28 février, avec des pics d'activité précédant des événements géopolitiques majeurs et des opérations militaires régionales.
*   Les pays visés correspondent à ceux ayant connu une activité de missiles significative linked à l'Iran.
*   L'infrastructure d'attaque utilise des VPN commerciaux et des serveurs virtuels, et est attribuée à des acteurs liés à l'Iran.
*   Le piratage est utilisé pour le soutien opérationnel et l'évaluation des dommages de combat (BDA).

**Vulnérabilités Ciblées (avec CVE) :**

*   **Hikvision :**
    *   CVE-2017-7921 : Authentification incorrecte
    *   CVE-2021-36260 : Injection de commandes
    *   CVE-2023-6895 : Injection de commandes OS
    *   CVE-2025-34067 : Exécution de code à distance non authentifiée
*   **Dahua :**
    *   CVE-2021-33044 : Contournement d'authentification

Des correctifs sont disponibles pour toutes ces vulnérabilités.

**Recommandations :**

*   **Limiter l'exposition publique :** Supprimer l'accès WAN direct aux caméras, les placer derrière un VPN ou une passerelle d'accès Zero Trust, et bloquer les redirections de port entrantes.
*   **Mots de passe robustes :** Changer les mots de passe par défaut et imposer des identifiants uniques.
*   **Gestion des correctifs :** Maintenir le firmware et le logiciel de gestion des caméras à jour. Remplacer les appareils obsolètes qui ne reçoivent plus de mises à jour de sécurité.
*   **Segmentation réseau :** Isoler les caméras sur un VLAN dédié, sans accès latéral aux réseaux d'entreprise ou OT. Contrôler strictement le trafic sortant.
*   **Surveillance et détection :** Surveiller les échecs de connexion répétés, les connexions à distance inhabituelles et les connexions sortantes atypiques des caméras.

---
[Source](https://research.checkpoint.com/2026/interplay-between-iranian-targeting-of-ip-cameras-and-physical-warfare-in-the-middle-east/){:target="_blank"}
