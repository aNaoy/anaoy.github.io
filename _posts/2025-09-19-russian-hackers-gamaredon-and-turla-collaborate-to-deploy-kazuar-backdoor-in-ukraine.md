---
title: 'Russian Hackers Gamaredon and Turla Collaborate to Deploy Kazuar Backdoor in Ukraine'
date: 2025-09-19
permalink: /posts/2025/09/19/russian-hackers-gamaredon-and-turla-collaborate-to-deploy-kazuar-backdoor-in-ukraine/
tags:
- veille-cyber
- hackernews
---
**Collaboration Russo-Ukrainienne dans la Cybersécurité : Gamaredon et Turla déploient le cheval de Troie Kazuar**

Des chercheurs en cybersécurité ont mis en évidence une collaboration entre deux groupes de pirates informatiques russes, Gamaredon et Turla, ciblant des entités en Ukraine. Gamaredon, également connu sous les noms de Aqua Blizzard et Armageddon, et Turla, aussi appelé Secret Blizzard et Venomous Bear, sont tous deux soupçonnés d'être affiliés au Service Fédéral de Sécurité de la Fédération de Russie (FSB).

Les analyses ont révélé que des outils développés par Gamaredon, tels que PteroGraphin, PteroOdd et PteroPaste, ont été utilisés pour déployer le cheval de Troie (backdoor) Kazuar de Turla sur des systèmes en Ukraine. Kazuar est un logiciel malveillant en .NET, régulièrement mis à jour, qui permet l'espionnage et l'accès à distance. Des versions récentes de Kazuar (v2 et v3) ont été détectées dans plusieurs attaques entre janvier et juin 2025.

Il est estimé que cette convergence d'activités malveillantes a été alimentée par l'invasion à grande échelle de l'Ukraine par la Russie en 2022, avec un accent particulier sur le secteur de la défense ukrainien. Gamaredon semble fournir l'accès initial aux systèmes, permettant ensuite à Turla d'installer et d'exécuter Kazuar. Ce dernier est capable de collecter diverses informations système et de les exfiltrer vers des serveurs contrôlés par les attaquants.

**Points clés :**

*   **Acteurs :** Groupes de pirates informatiques russes Gamaredon et Turla.
*   **Cible :** Entités en Ukraine, notamment le secteur de la défense.
*   **Outil principal :** Cheval de Troie (backdoor) Kazuar (versions v2 et v3).
*   **Outils d'assistance par Gamaredon :** PteroGraphin, PteroOdd, PteroPaste.
*   **Mécanismes :** Déploiement via des téléchargeurs PowerShell, utilisation de l'API Telegraph et potentiellement de Cloudflare Workers pour la communication C2 et l'exfiltration de données.
*   **Contexte :** Potentielle intensification des cyberattaques suite à l'invasion russe de l'Ukraine.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec un identifiant CVE n'est explicitement mentionnée dans l'article. L'article se concentre sur les campagnes de déploiement de logiciels malveillants et la collaboration entre acteurs malveillants plutôt que sur l'exploitation de failles de sécurité précises.

**Recommandations :**

Bien que l'article ne fournisse pas de recommandations directes, il implique la nécessité de :

*   **Renforcer la sécurité des endpoints :** Détection et suppression des logiciels malveillants comme Kazuar.
*   **Surveillance du réseau :** Détection des communications C2 suspectes et de l'exfiltration de données.
*   **Sensibilisation aux menaces :** Formation des utilisateurs à reconnaître les tentatives de spear-phishing et les vecteurs d'infection potentiels (comme les LNK files sur les lecteurs amovibles).
*   **Mise à jour des systèmes et des logiciels :** Bien que non mentionné, c'est une pratique générale essentielle pour réduire la surface d'attaque.
*   **Analyse des comportements des acteurs :** Comprendre les méthodes et les outils utilisés par Gamaredon et Turla pour anticiper leurs futures tactiques.

---
[Source](https://thehackernews.com/2025/09/russian-hackers-gamaredon-and-turla.html){:target="_blank"}
