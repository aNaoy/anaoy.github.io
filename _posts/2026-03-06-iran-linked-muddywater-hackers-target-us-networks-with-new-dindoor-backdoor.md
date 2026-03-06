---
title: 'Iran-Linked MuddyWater Hackers Target U.S. Networks With New Dindoor Backdoor'
date: 2026-03-06
permalink: /posts/2026/03/06/iran-linked-muddywater-hackers-target-us-networks-with-new-dindoor-backdoor/
tags:
- veille-cyber
- hackernews
---
### Intensification des cyberopérations iraniennes : Menaces et nouvelles tactiques

Dans un contexte de fortes tensions géopolitiques, le groupe de hackers lié à l'État iranien **MuddyWater** (alias Seedworm) cible activement des réseaux américains (banques, aéroports, secteurs de la défense). Ces opérations, qui s'inscrivent dans une stratégie de représailles plus large, s'appuient sur des techniques éprouvées comme l'ingénierie sociale, le phishing et l'exploitation de vulnérabilités connues.

**Points clés :**
*   **Nouveaux outils :** Utilisation de la porte dérobée *Dindoor* (basée sur Deno) pour l'accès initial et *Fakeset* (Python) pour la persistance.
*   **Objectifs stratégiques :** Collecte de renseignements, surveillance via des caméras IP compromises pour évaluer les dégâts physiques, et déploiement potentiel de logiciels malveillants destructeurs (*wiper*).
*   **Vecteurs d'attaque :** Exploitation récurrente de périphériques IoT (caméras Dahua/Hikvision) et recours à des utilitaires légitimes comme Rclone pour l'exfiltration de données.

**Vulnérabilités exploitées :**
Les attaquants tirent profit de failles critiques dans les systèmes de surveillance et équipements de réseau :
*   **CVE-2017-7921** et **CVE-2023-6895** (Hikvision)
*   **CVE-2021-36260**, **CVE-2021-33044** et **CVE-2025-34067** (Dahua/Hikvision)

**Recommandations de sécurité :**
*   **Renforcement de l'authentification :** Déployer une authentification multifacteur (MFA) résistante au phishing.
*   **Réduction de la surface d'attaque :** Limiter l'exposition sur Internet, désactiver l'accès distant aux systèmes de technologie opérationnelle (OT) et isoler les réseaux critiques.
*   **Gestion des correctifs :** Maintenir à jour les passerelles VPN, les applications exposées et les dispositifs en périphérie de réseau.
*   **Résilience des données :** Maintenir des sauvegardes hors ligne pour contrer les campagnes de type « wiper ».
*   **Surveillance accrue :** Porter une vigilance particulière aux indicateurs de compromission liés aux outils d'administration système utilisés détournés par les attaquants.

---
[Source](https://thehackernews.com/2026/03/iran-linked-muddywater-hackers-target.html){:target="_blank"}
