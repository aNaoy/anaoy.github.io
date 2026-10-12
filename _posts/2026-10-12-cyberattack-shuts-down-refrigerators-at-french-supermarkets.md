---
title: 'Cyberattack shuts down refrigerators at French supermarkets'
date: 2026-10-12
permalink: /posts/2026/10/12/cyberattack-shuts-down-refrigerators-at-french-supermarkets/
tags:
- veille-cyber
- bleepingcomp
---
### Cyberattaque massive contre la chaîne du froid en France

Une cyberattaque coordonnée a visé les systèmes de réfrigération de plusieurs grandes enseignes de la grande distribution française (Intermarché, Carrefour, Leclerc, Super U, Monoprix). En piratant les contrôleurs Danfoss, les attaquants ont déclenché à distance le mode de dégivrage automatique, provoquant une hausse des températures interne jusqu'à 50°C. Entre 250 et 350 magasins ont été impactés, entraînant des pertes financières importantes et le gaspillage massif de produits frais.

**Points clés :**
*   **Cible :** Systèmes de gestion de réfrigération (HVAC) de la marque Danfoss.
*   **Impact :** Rupture de la chaîne du froid, pertes de denrées alimentaires et ouverture d'une enquête par le parquet de Paris.
*   **Exposition :** Une analyse technique a révélé que près de 1 600 systèmes Danfoss sont exposés directement sur Internet en France.

**Vulnérabilité exploitée :**
*   **CVE-2025-41450 :** Une faille de haute gravité permettant le contournement de l'authentification sur la plateforme matérielle Danfoss AK-SM 8xxA, signalée par la CISA en mai 2025.

**Recommandations :**
*   **Déconnexion :** Retirer immédiatement les contrôleurs de réfrigération de l'exposition directe sur Internet.
*   **Mise à jour :** Appliquer les correctifs de sécurité fournis par le constructeur pour corriger la vulnérabilité d'authentification.
*   **Segmentation :** Isoler les systèmes industriels (OT) des réseaux bureautiques et sécuriser les accès distants via des VPN avec authentification multifacteur (MFA).
*   **Surveillance :** Mettre en place un monitoring strict des logs d'accès pour détecter toute activité anormale sur les consoles de gestion thermique.

---
[Source](https://www.bleepingcomputer.com/news/security/cyberattack-shuts-down-refrigerators-at-french-supermarkets/){:target="_blank"}
