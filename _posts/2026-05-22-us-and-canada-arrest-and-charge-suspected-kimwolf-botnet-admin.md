---
title: 'US and Canada arrest and charge suspected Kimwolf botnet admin'
date: 2026-05-22
permalink: /posts/2026/05/22/us-and-canada-arrest-and-charge-suspected-kimwolf-botnet-admin/
tags:
- veille-cyber
- bleepingcomp
---
### Démantèlement du botnet KimWolf : arrestation de son administrateur

Les autorités américaines et canadiennes ont arrêté Jacob Butler, un ressortissant canadien de 23 ans, soupçonné d'être l'administrateur du botnet KimWolf. Ce réseau malveillant, fonctionnant sur un modèle de « cybercriminalité à la demande » (DDoS-for-hire), a compromis près de deux millions d'appareils connectés (objets IoT, caméras, boîtiers Android, cadres photo numériques).

**Points clés :**
* **Envergure :** Le botnet a été utilisé pour lancer plus de 25 000 attaques DDoS, atteignant des records de puissance de 30 térabits par seconde.
* **Impact :** Les cibles incluaient des infrastructures critiques, notamment celles du département de la Défense américain, générant plus d'un million de dollars de pertes financières.
* **Coopération internationale :** L'arrestation fait suite à une opération coordonnée en mars 2026 visant à saisir les infrastructures de commande et de contrôle de quatre botnets majeurs (KimWolf, Aisuru, JackSkid et Mossad), totalisant plus de 3 millions d'appareils infectés.
* **Action judiciaire :** 45 plateformes DDoS-for-hire ont été neutralisées parallèlement aux saisies de domaines par le département de la Justice américain.

**Vulnérabilités :**
L'article souligne l'exploitation massive de dispositifs IoT via des vulnérabilités dans les réseaux de proxys résidentiels, permettant aux attaquants de détourner des appareils légitimes pour masquer leur trafic et étendre le botnet. Bien qu'aucune CVE spécifique ne soit citée, ces botnets exploitent généralement :
* L'absence de mise à jour logicielle des objets connectés.
* L'utilisation de mots de passe par défaut.
* Des failles de configuration dans les services de proxy et les accès distants des terminaux Android et IoT.

**Recommandations :**
* **Sécurisation des terminaux :** Modifier systématiquement les identifiants et mots de passe par défaut sur tous les équipements connectés au réseau domestique ou professionnel.
* **Mises à jour :** Appliquer régulièrement les correctifs de sécurité fournis par les constructeurs pour les appareils IoT et Android.
* **Segmentation réseau :** Isoler les objets connectés (IoT) sur des réseaux locaux distincts afin de limiter les mouvements latéraux en cas de compromission d'un appareil.
* **Vigilance proxy :** Surveiller les configurations de sortie de trafic pour éviter que les dispositifs ne deviennent des nœuds de rebond (proxys résidentiels) pour des réseaux malveillants.

---
[Source](https://www.bleepingcomputer.com/news/security/us-and-canada-arrest-and-charge-suspected-kimwolf-botnet-admin/){:target="_blank"}
