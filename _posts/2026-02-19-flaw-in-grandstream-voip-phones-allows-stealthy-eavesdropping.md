---
title: 'Flaw in Grandstream VoIP phones allows stealthy eavesdropping'
date: 2026-02-19
permalink: /posts/2026/02/19/flaw-in-grandstream-voip-phones-allows-stealthy-eavesdropping/
tags:
- veille-cyber
- bleepingcomp
---
### Accès non authentifié aux téléphones VoIP Grandstream pour écoute clandestine

Une vulnérabilité critique dans la série de téléphones VoIP Grandstream GXP1600 permet à un attaquant distant non authentifié de prendre le contrôle total de l'appareil. Cette faille, identifiée comme CVE-2026-2329, octroie des privilèges root et permet l'écoute clandestine des communications sans laisser de trace. Les entreprises utilisant ces appareils, notamment pour les communications internes, sont particulièrement exposées.

#### Points Clés:

*   **Impact:** Prise de contrôle à distance, écoute clandestine des appels, vol d'identifiants.
*   **Mode d'exploitation:** Silencieux, ne perturbant pas le fonctionnement normal de l'appareil.
*   **Ciblage:** L'attaquant peut atteindre les appareils même s'ils ne sont pas directement exposés sur Internet, en pivotant depuis un autre appareil sur le réseau local.

#### Vulnérabilités:

*   **CVE-2026-2329:** Une vulnérabilité de débordement de tampon sur la pile (stack buffer overflow) dans le service API web de l'appareil (/cgi-bin/api.values.get). L'API accepte un paramètre `request` qui est copié dans un tampon sans vérification de longueur suffisante, permettant à un attaquant de provoquer un débordement et d'écraser la mémoire adjacente pour exécuter du code arbitraire. La difficulté d'exploitation est atténuée par une technique permettant d'écrire plusieurs octets nuls pour construire une chaîne d'exécution de code.

#### Appareils Affectés:

La vulnérabilité affecte les modèles suivants de la série GXP1600 utilisant une version de firmware antérieure à 1.0.7.81 :
*   GXP1610
*   GXP1615
*   GXP1620
*   GXP1625
*   GXP1628
*   GXP1630

#### Recommandations:

*   **Mise à jour du firmware:** Appliquer la version de firmware 1.0.7.81 ou une version ultérieure sur tous les appareils Grandstream GXP1600 concernés.
*   **Sécurisation du réseau:** Mettre en œuvre des mesures de sécurité réseau pour limiter l'accès aux appareils VoIP et empêcher les mouvements latéraux d'attaquants.

---
[Source](https://www.bleepingcomputer.com/news/security/flaw-in-grandstream-voip-phones-allows-stealthy-eavesdropping/){:target="_blank"}
