---
title: 'Why CISOs Struggle to Answer the Boards Three Hardest Questions, and How to Fix the Report'
date: 2026-10-02
permalink: /posts/2026/10/02/why-cisos-struggle-to-answer-the-boards-three-hardest-questions-and-how-to-fix-the-report/
tags:
- veille-cyber
- hackernews
---
### Transformer le reporting du RSSI pour le Conseil d'administration

Les rapports de sécurité basés sur des indicateurs d'activité (nombre de vulnérabilités corrigées, alertes traitées) ne permettent pas au conseil d'administration d'évaluer le risque réel. La fragmentation des outils de sécurité empêche une vision globale, masquant des chemins d'attaque critiques qui exploitent des vulnérabilités mineures combinées.

**Points clés :**
* **Limites de l'approche actuelle :** Les outils de sécurité (identité, cloud, EDR, SaaS) fonctionnent en silos et ne communiquent pas entre eux, rendant invisible la corrélation entre les menaces.
* **Nouvelle approche :** Adopter une architecture de type "Cybersecurity Mesh" pour corréler les données existantes.
* **Changement de paradigme :** Passer d'une mesure des efforts (quantité de patches) à une mesure de l'exposition financière liée aux chemins d'attaque menant aux actifs critiques ("Crown Jewels").

**Vulnérabilités :**
L'article ne liste pas de CVE spécifiques, mais souligne que le risque majeur provient de la **combinaison de configurations jugées "faibles" ou "modérées"** par différents outils. Ce sont ces enchaînements (ex: compte contractuel mal provisionné + accès OAuth + permissions de stockage excessives) qui constituent des chemins d'attaque critiques, plutôt qu'une vulnérabilité CVE isolée.

**Recommandations :**
1. **Identifier les actifs critiques :** Définir avec les métiers ce qui a le plus d'impact en cas de compromission.
2. **Unifier le contexte :** Utiliser une couche d'intelligence commune (CSMA) pour corréler les données sans remplacer les outils existants.
3. **Cartographier les chemins d'attaque :** Visualiser les accès réels vers les actifs critiques plutôt que de lister les vulnérabilités par outil.
4. **Prioriser par "rayon d'explosion" :** Classer la remédiation selon la criticité des actifs menacés et non selon le score de sévérité brut des vulnérabilités.
5. **Convertir le risque en monnaie :** Présenter l'exposition financière pour parler le langage du conseil d'administration.
6. **Suivre les tendances :** Démontrer la réduction du nombre de chemins d'attaque d'un trimestre à l'autre pour prouver le retour sur investissement (ROI) de la sécurité.

---
[Source](https://thehackernews.com/2026/10/why-cisos-struggle-to-answer-boards.html){:target="_blank"}
