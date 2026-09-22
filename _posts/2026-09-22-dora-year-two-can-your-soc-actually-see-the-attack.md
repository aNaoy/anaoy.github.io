---
title: 'DORA Year Two: Can Your SOC Actually See the Attack?'
date: 2026-09-22
permalink: /posts/2026/09/22/dora-year-two-can-your-soc-actually-see-the-attack/
tags:
- veille-cyber
- hackernews
---
### DORA : Passer de la conformité théorique à la visibilité opérationnelle

La deuxième année de mise en œuvre de la loi sur la résilience opérationnelle numérique (DORA) dans l'Union européenne exige que les institutions financières prouvent l'efficacité réelle de leurs cadres de sécurité, au-delà de la simple documentation administrative. Le défi majeur pour les centres opérationnels de sécurité (SOC) est de maintenir une visibilité suffisante pour détecter et contenir les intrusions complexes.

**Points clés :**
*   **Surveillance continue (Article 9) :** La conformité dépasse le simple inventaire des actifs. Il est crucial de surveiller les communications entre systèmes, incluant les infrastructures héritées et les appareils non gérés, pour identifier les écarts de comportement.
*   **Détection et réponse (Article 10) :** La multiplication des alertes isolées (EDR, gestion des accès) nécessite une corrélation contextuelle. Les données réseau permettent de relier ces événements pour identifier les déplacements latéraux et les communications de commande et de contrôle.
*   **Risques tiers (Articles 28-30) :** Les contrats ne suffisent pas à sécuriser les accès fournisseurs. Une surveillance réseau est nécessaire pour vérifier si les connexions des tiers respectent les périmètres autorisés.
*   **Exigences de reporting :** La capacité à évaluer rapidement l'impact d'un incident est primordiale pour respecter les délais stricts de notification (4 heures pour les incidents majeurs, 24 heures pour la déclaration initiale).

**Vulnérabilités :**
L'article ne mentionne pas de CVE spécifiques, mais souligne des vulnérabilités structurelles :
*   Zones d'ombre dans les environnements hybrides (legacy, systèmes spécialisés).
*   Manque de corrélation entre les sources de données silotées.
*   Compromission d'identifiants légitimes de tiers, indétectable par les contrôles d'accès classiques.

**Recommandations :**
*   **Adopter une solution de NDR (Network Detection and Response) :** Utiliser la télémétrie réseau pour établir des bases de comportement normal et identifier les anomalies de timing, de volume ou de directionnalité.
*   **Privilégier les données structurées :** Extraire des données au niveau des protocoles pour permettre aux analystes (ou à l'IA) de reconstruire les incidents avec précision.
*   **Contextualiser les alertes :** Centraliser l'analyse pour passer de la gestion de bruit à la compréhension de la chaîne d'attaque réelle.
*   **Tester les contrôles :** Valider par des données réseau réelles si les accès des tiers correspondent aux périmètres documentés dans les contrats.

---
[Source](https://thehackernews.com/2026/09/dora-year-two-can-your-soc-actually-see.html){:target="_blank"}
