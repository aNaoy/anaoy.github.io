---
title: 'Microsoft blames massive Microsoft 365 outage on maintenance bug'
date: 2026-07-24
permalink: /posts/2026/07/24/microsoft-blames-massive-microsoft-365-outage-on-maintenance-bug/
tags:
- veille-cyber
- bleepingcomp
---
### Panne majeure des services Microsoft 365 et Azure : Origine et résolution

Une défaillance technique survenue le 23 juillet 2024 a entraîné une interruption massive des services Microsoft 365 et Azure, principalement localisée dans la région "West US". L'incident, identifié sous la référence MO1437424, a causé des problèmes de connectivité, des latences accrues et une impossibilité d'accès à de nombreux outils critiques.

**Points clés :**
*   **Cause racine :** Un bug dans le système automatisé de gestion de la maintenance réseau. Lors d'une opération routinière, le processus a incorrectement interprété les instructions, supprimant des routes IP sur un nombre de périphériques bien plus élevé que prévu.
*   **Services impactés :** L'incident a touché un large éventail d'outils, notamment SharePoint, OneDrive, Microsoft Teams, Power Automate, Copilot, ainsi que des services Azure (Kubernetes, SQL, VPN Gateway, etc.).
*   **Chronologie :** La panne a débuté à 10h44 ET. Après avoir tenté des redirections de trafic, Microsoft a annulé la modification réseau à 14h26 ET, permettant un rétablissement complet des services à 15h41 ET.

**Vulnérabilités :**
*   Aucune CVE n'est associée à cet incident, car il s'agit d'une défaillance logicielle interne au processus de maintenance automatisée et non d'une exploitation malveillante. 
*   La vulnérabilité réside dans une lacune des contrôles de sécurité et de validation du système de gestion automatisé ("safety checks"), qui n'a pas empêché l'application d'une configuration réseau critique erronée.

**Recommandations :**
*   **Pour les entreprises :** Il est impératif de réévaluer régulièrement les plans de continuité d'activité (PCA) et de reprise après sinistre (PRA) afin de garantir une résilience face à l'indisponibilité prolongée des services Cloud.
*   **Pour Microsoft :** L'entreprise a annoncé l'ouverture d'une enquête interne approfondie pour renforcer les processus de vérification de sécurité des déploiements automatisés et prévenir toute répétition d'une telle erreur humaine ou systémique.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-blames-massive-microsoft-365-outage-on-maintenance-bug/){:target="_blank"}
