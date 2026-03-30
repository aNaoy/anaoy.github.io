---
title: 'Three China-Linked Clusters Target Southeast Asian Government in 2025 Cyber Campaign'
date: 2026-03-30
permalink: /posts/2026/03/30/three-china-linked-clusters-target-southeast-asian-government-in-2025-cyber-campaign/
tags:
- veille-cyber
- hackernews
---
### Campagne d'espionnage coordonnée contre un gouvernement en Asie du Sud-Est

En 2025, une organisation gouvernementale d'Asie du Sud-Est a été la cible d'une opération d'espionnage complexe impliquant trois groupes distincts liés à la Chine : **Mustang Panda**, **CL-STA-1048** (Earth Estries/Crimson Palace) et **CL-STA-1049** (Unfading Sea Haze). Cette convergence d'activités suggère une coordination stratégique visant à établir un accès persistant à long terme pour le vol de données sensibles.

**Points clés :**
*   **Objectif :** Exfiltration de données et maintien d'un accès durable au réseau.
*   **Techniques :** Utilisation intensive de logiciels malveillants variés, de portes dérobées (backdoors) et de techniques de *DLL side-loading*.
*   **Vecteurs d'infection :** L'usage de supports USB infectés par le malware HIUPAN a été identifié pour Mustang Panda. Le vecteur d'accès initial pour les autres groupes reste indéterminé.
*   **Logiciels malveillants identifiés :** HIUPAN, PUBLOAD, EggStremeFuel/Loader, MASOL RAT, PoshRAT, TrackBak Stealer, Hypnosis Loader, FluffyGh0st et COOLCLIENT.

**Vulnérabilités :**
L'article ne mentionne pas de CVE spécifique, mais met en évidence l'utilisation récurrente de **DLL side-loading** (exécution de code malveillant via une bibliothèque légitime détournée) pour contourner les défenses.

**Recommandations :**
*   **Sécurisation des ports USB :** Désactiver ou restreindre strictement l'utilisation des périphériques USB sur les postes de travail sensibles afin de bloquer les vecteurs de type HIUPAN.
*   **Surveillance des DLL :** Mettre en place des mesures de détection contre le chargement anormal de DLL (side-loading) dans les répertoires d'applications.
*   **Analyse du trafic réseau :** Surveiller les communications vers des services cloud tiers (notamment Dropbox, utilisé par EggStremeLoader) et les flux de données sortants inhabituels vers des serveurs de commande et contrôle (C2) inconnus.
*   **Détection d'outils d'administration :** Renforcer la surveillance sur l'exécution d'outils de RAT (Remote Access Trojan) connus, tels que MASOL ou FluffyGh0st, via des solutions EDR (Endpoint Detection and Response).

---
[Source](https://thehackernews.com/2026/03/three-china-linked-clusters-target.html){:target="_blank"}
