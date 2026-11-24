---
title: 'Volant Manticore: Flying Under the Radar'
date: 2026-11-24
permalink: /posts/2026/11/24/volant-manticore-flying-under-the-radar/
tags:
- veille-cyber
- zerodaysfans
---
### Volant Manticore : Une nouvelle menace persistante liée à l'Iran

**Points clés**
* **Volant Manticore** est un groupe de cyberespionnage nouvellement identifié, probablement composé d'anciens opérateurs du groupe *MuddyWater* et lié au Ministère iranien du renseignement et de la sécurité (MOIS).
* Bien que partageant des outils et des tactiques avec *MuddyWater*, le groupe se distingue par une indépendance opérationnelle, des implants personnalisés et un ciblage régional spécifique, initialement centré sur Chypre (télécommunications, compagnies aériennes, infrastructures critiques).
* Depuis septembre 2026, le groupe a intensifié ses opérations vers l'Arabie saoudite, visant notamment le secteur de la santé, en réaction aux tensions géopolitiques avec les Houthis soutenus par l'Iran.

**Vulnérabilités et outils utilisés**
* **KuboShell :** Une porte dérobée (backdoor) 64 bits pour Windows qui utilise le système IPFS (*InterPlanetary File System*) pour le contrôle et commande (C2), s'appuyant sur le service de "pinning" *Pinata*.
* **Homa Framework :** Un framework post-compromission multi-étapes. Il s'agit d'une réimplémentation en JavaScript du client *MuddyC2Go* de *MuddyWater*.
* **Outils RMM :** Utilisation intensive d'outils d'administration à distance (MeshCentral, N-able, NetLock RMM) pour maintenir l'accès.
* **Techniques de phishing :** Usurpation d'identité via de faux CV (ex: "Athena Marinou") ou des thématiques liées à la santé et au secteur militaire pour infiltrer les cibles.

**Recommandations**
* **Surveillance du trafic :** Détecter les connexions inhabituelles vers les services de pinning IPFS (comme les gateways Pinata) et les outils RMM légitimes non autorisés sur le réseau.
* **Durcissement des accès VPN :** Les opérateurs utilisent des accès VPN compromis (ex: Fortinet SSL VPN) pour pénétrer les réseaux. L'authentification multi-facteurs (MFA) est indispensable.
* **Analyse comportementale :** Surveiller les processus suspects lancés via PowerShell, notamment ceux contournant les politiques d'exécution (*execution-policy bypass*).
* **Gestion des macros :** Bloquer les macros dans les documents Office provenant de sources externes pour prévenir l'exécution de code malveillant initial.
* **Vigilance sectorielle :** Les organisations dans les secteurs de la santé, de l'énergie et de la défense, particulièrement à Chypre et en Arabie saoudite, doivent renforcer leurs mesures de détection contre les campagnes de spear-phishing à thématique professionnelle.

*(Note : Aucun identifiant CVE spécifique n'a été associé à cette menace dans l'article, celle-ci exploitant principalement des vecteurs de phishing et des outils d'administration détournés plutôt que des vulnérabilités logicielles identifiées.)*

---
[Source](https://research.checkpoint.com/2026/volant-manticore-flying-under-the-radar/){:target="_blank"}
