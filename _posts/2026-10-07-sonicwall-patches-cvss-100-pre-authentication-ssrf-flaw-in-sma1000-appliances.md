---
title: 'SonicWall Patches CVSS 10.0 Pre-Authentication SSRF Flaw in SMA1000 Appliances'
date: 2026-10-07
permalink: /posts/2026/10/07/sonicwall-patches-cvss-100-pre-authentication-ssrf-flaw-in-sma1000-appliances/
tags:
- veille-cyber
- hackernews
---
### Alerte de sécurité critique : Vulnérabilités critiques dans les passerelles SonicWall SMA1000

SonicWall a publié des correctifs de sécurité pour quatre vulnérabilités affectant ses passerelles d'accès distant SMA1000 (modèles 6210, 7210 et 8200v). La faille la plus sévère permet à un attaquant non authentifié d'exécuter des opérations non autorisées sur les fonctions internes de l'appareil. Aucune preuve d'exploitation active n'a été constatée à ce jour.

**Points clés :**
*   **Impact :** La vulnérabilité principale (SSRF) peut être exploitée sans aucune authentification préalable.
*   **Périmètre :** Les modèles SMA1000 sont concernés. Les gammes SMA 100 et les firewalls SSL-VPN ne sont pas affectés.
*   **Historique :** Il s'agit de la troisième série de failles critiques de type SSRF sur ces équipements cette année.

**Vulnérabilités identifiées :**

| CVE | Type de vulnérabilité | Accès requis | Score CVSS |
| :--- | :--- | :--- | :--- |
| **CVE-2026-102255** | Server-side request forgery (SSRF) | Aucun | 10.0 |
| **CVE-2026-102256** | Injection de commande OS (RCE) | Administrateur | 7.8 |
| **CVE-2026-102257** | Zip Slip (RCE possible) | Utilisateur | 7.2 |
| **CVE-2026-102258** | Cross-site scripting (XSS) stocké | Administrateur | 5.5 |

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs via le portail *MySonicWall*. 
    *   **Version 12.4.3 :** Migrer vers la version **12.4.3-03670** ou supérieure.
    *   **Version 12.5.0 :** Migrer vers la version **12.5.0-03082** ou supérieure.
*   **Note importante :** Les versions précédemment considérées comme "corrigées" au 1er septembre 2026 sont désormais obsolètes et doivent être mises à jour avec les nouveaux correctifs.
*   **Redémarrage :** L'installation des correctifs nécessite un redémarrage de l'équipement.

---
[Source](https://thehackernews.com/2026/10/sonicwall-patches-cvss-100-pre.html){:target="_blank"}
