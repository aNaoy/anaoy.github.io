---
title: 'Interplay between Iranian Targeting of IP Cameras and Physical Warfare in the Middle East'
date: 2026-03-04
permalink: /posts/2026/03/04/interplay-between-iranian-targeting-of-ip-cameras-and-physical-warfare-in-the-middle-east/
tags:
- veille-cyber
- zerodaysfans
---
### Surveillance Ciblée : Indicateur d'Activité Iranienne dans le Conflit au Moyen-Orient

Une intensification de la compromission des caméras IP de fabricants spécifiques, attribuée à des acteurs affiliés à l'Iran, a été observée. Ces attaques coïncident avec des périodes de tensions géopolitiques et d'activité militaire dans la région, notamment en Israël, au Qatar, à Bahreïn, au Koweït, aux Émirats arabes unis, à Chypre et au Liban. Ces actions suggèrent une utilisation de la compromission des caméras pour le soutien opérationnel, l'évaluation des dommages de combat (BDA) et potentiellement la correction de cibles avant des opérations de missiles. L'activité de ciblage des caméras peut donc servir d'indicateur précoce d'une potentielle action cinétique.

**Points Clés :**

*   Des attaques ciblées contre des caméras IP de marques spécifiques ont été observées à partir du 28 février, émanant d'infrastructures attribuées à des acteurs iraniens.
*   Ces ciblages s'étendent à plusieurs pays du Moyen-Orient et à Chypre, souvent parallèlement à une activité de missiles liée à l'Iran.
*   Des activités antérieures similaires ont été détectées, notamment en janvier, en lien avec des événements géopolitiques majeurs pour l'Iran.
*   L'exploitation de vulnérabilités connues sur des caméras Hikvision et Dahua est privilégiée.
*   La compromission des caméras est perçue comme un outil soutenant les opérations militaires et l'évaluation des dommages.

**Vulnérabilités Ciblées (avec CVE) :**

*   **Hikvision :**
    *   CVE-2017-7921 (Authentification insuffisante)
    *   CVE-2021-36260 (Injection de commandes)
    *   CVE-2023-6895 (Injection de commandes OS)
    *   CVE-2025-34067 (Exécution de code à distance sans authentification)
*   **Dahua :**
    *   CVE-2021-33044 (Contournement d'authentification)

*Note : Des correctifs sont disponibles pour toutes les vulnérabilités listées.*

**Recommandations pour la Défense :**

*   **Limiter l'exposition publique :** Supprimer l'accès WAN direct aux caméras/NVRs, les placer derrière un VPN ou une passerelle d'accès Zero Trust, et bloquer les redirections de ports entrants.
*   **Utiliser des identifiants forts :** Changer les mots de passe par défaut et exiger des identifiants uniques.
*   **Gestion des correctifs :** Maintenir à jour les firmwares des caméras/NVRs et les logiciels de gestion. Remplacer les appareils obsolètes qui ne reçoivent plus de mises à jour de sécurité.
*   **Segmentation réseau :** Isoler les caméras sur un VLAN dédié sans accès latéral aux réseaux d'entreprise ou OT. Contrôler strictement le trafic sortant.
*   **Surveillance et détection :** Surveiller les échecs de connexion répétés, les connexions à distance inhabituelles et les connexions sortantes anormales initiées par les caméras.

---
[Source](https://research.checkpoint.com/2026/interplay-between-iranian-targeting-of-ip-cameras-and-physical-warfare-in-the-middle-east/){:target="_blank"}
