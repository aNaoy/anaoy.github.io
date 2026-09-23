---
title: 'ShinyHunters Claims FBI Breach, Says It Stole Data on Agents and Job Applicants'
date: 2026-09-23
permalink: /posts/2026/09/23/shinyhunters-claims-fbi-breach-says-it-stole-data-on-agents-and-job-applicants/
tags:
- veille-cyber
- hackernews
---
### Cyberattaque contre le FBI : ShinyHunters revendique le vol de données sensibles

Le groupe de cybercriminels **ShinyHunters** affirme avoir compromis les systèmes du FBI, prétendant détenir des informations sensibles sur l'ensemble des agents et des candidats ayant postulé à l'agence. Cette offensive constituerait une mesure de rétorsion suite à une annonce publique du FBI dénonçant leurs activités passées.

**Points clés :**
*   **Périmètre compromis :** Les services de justice pénale, les ressources humaines et les plateformes internes (dont Medlink) auraient été touchés.
*   **Mode opératoire :** Les attaquants affirment avoir exploité une vulnérabilité « zero-day » dans **Oracle PeopleSoft** pour obtenir une exécution de code à distance (RCE).
*   **Motivation :** Une réponse provocatrice à une campagne de dénigrement orchestrée par les autorités américaines à l'encontre du groupe.
*   **Analyse d'experts :** La résilience de ShinyHunters et leur capacité à évoluer (social engineering, abus de jetons OAuth) placent cette attaque parmi les plus significatives contre une agence fédérale.

**Vulnérabilités identifiées :**
*   **CVE-2026-35273 :** Faille exploitée précédemment par le groupe dans Oracle PeopleSoft, utilisée comme référence technique pour cette nouvelle intrusion.

**Recommandations :**
*   **Sécurisation des identités :** Renforcer la surveillance des chemins d'identité privilégiés, particulièrement les jetons d'intégration SaaS et les applications OAuth, vecteurs privilégiés des attaquants.
*   **Gestion des accès :** Mettre en œuvre une protection rigoureuse contre l'ingénierie sociale ciblant les centres de support (help-desk).
*   **Veille Oracle :** Appliquer les correctifs de sécurité critiques pour les infrastructures Oracle PeopleSoft dès leur publication pour prévenir l'exploitation de failles de type RCE.
*   **Réponse aux incidents :** Maintenir une surveillance accrue sur les vecteurs d'accès tiers, car les cybercriminels délaissent désormais les périmètres techniques classiques au profit des relations de confiance tierces.

---
[Source](https://thehackernews.com/2026/09/shinyhunters-claims-fbi-breach-says-it.html){:target="_blank"}
