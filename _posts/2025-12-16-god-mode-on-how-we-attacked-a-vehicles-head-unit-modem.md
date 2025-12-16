---
title: 'God Mode On: how we attacked a vehicle’s head unit modem'
date: 2025-12-16
permalink: /posts/2025/12/16/god-mode-on-how-we-attacked-a-vehicles-head-unit-modem/
tags:
- veille-cyber
- securelist
---
**Détournement d'un modem de véhicule pour le contrôle à distance**

Une recherche de sécurité a démontré la possibilité d'exécuter du code arbitraire sur le modem intégré des unités multimédias de véhicules modernes, ouvrant la voie à un contrôle à distance complet du système. L'étude s'est concentrée sur le SoC Unisoc UIS7862A, présent dans des unités multimédias automobiles.

**Points clés et vulnérabilités :**

*   **Exécution de code à distance sur le modem (CVE-2024-39432) :** Une vulnérabilité de débordement de tampon de pile a été découverte dans l'implémentation du protocole RLC 3G. Cette faille, exploitable via un seul paquet, permet à un attaquant d'exécuter du code sur le modem avant l'activation des mécanismes de protection. La vulnérabilité réside dans la gestion des fragments de données (SDU) où le nombre d'en-têtes optionnels dans un paquet peut dépasser la capacité de la pile, permettant ainsi d'écraser l'adresse de retour et d'autres registres.
*   **Accès aux privilèges administrateur sur le processeur d'application (AP) :** Une fois le contrôle du modem obtenu, les chercheurs ont trouvé des moyens d'accéder au processeur d'application (AP), qui exécute généralement le système d'exploitation du véhicule (comme Android).
*   **Utilisation d'une faille matérielle :** Une vulnérabilité matérielle liée à un périphérique Direct Memory Access (DMA) caché a été exploitée pour permettre le mouvement latéral au sein du SoC.
*   **Patching du noyau Android :** En exploitant le DMA caché, il a été possible d'installer un patch personnalisé dans le noyau Android en cours d'exécution, accordant ainsi des privilèges les plus élevés sur l'AP.

**Recommandations :**

Bien que l'article ne détaille pas explicitement les recommandations pour les fabricants, les implications de cette recherche suggèrent la nécessité de :

*   **Renforcer la sécurité des modems :** Examiner et corriger les vulnérabilités dans les implémentations des protocoles de communication bas niveau.
*   **Sécuriser l'interaction entre le modem et le processeur d'application :** Mettre en place des mécanismes de contrôle d'accès stricts et des isolements entre ces deux composants critiques du SoC.
*   **Auditer les composants matériels :** Identifier et corriger les vulnérabilités matérielles, telles que les périphériques DMA cachés.
*   **Mises à jour régulières du firmware :** Assurer la disponibilité et le déploiement rapide de mises à jour de sécurité pour les firmwares des modems et des systèmes d'exploitation des unités multimédias.
*   **Tests de sécurité approfondis :** Effectuer des évaluations de sécurité rigoureuses sur l'ensemble de la chaîne d'approvisionnement logicielle et matérielle des véhicules.

---
[Source](https://securelist.com/attacking-car-modem/118463/){:target="_blank"}
