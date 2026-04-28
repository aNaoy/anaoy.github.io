---
title: 'Chinese Silk Typhoon Hacker Extradited to U.S. Over COVID Research Cyberattacks'
date: 2026-04-28
permalink: /posts/2026/04/28/chinese-silk-typhoon-hacker-extradited-to-us-over-covid-research-cyberattacks/
tags:
- veille-cyber
- hackernews
---
### Extradition d'un hacker lié au groupe Silk Typhoon pour espionnage industriel

Xu Zewei, un ressortissant chinois accusé d'appartenir au groupe de cyberespionnage "Silk Typhoon", a été extradé d'Italie vers les États-Unis. Il est poursuivi pour des cyberattaques menées entre 2020 et 2021, sous la direction du Bureau de sécurité de l'État de Shanghai, visant notamment des institutions américaines de recherche sur les vaccins contre le COVID-19.

**Points clés :**
* **Cibles :** Universités, immunologistes et virologues américains impliqués dans la recherche sur le COVID-19.
* **Mode opératoire :** Utilisation de sociétés écrans (« entreprises habilitantes ») pour couvrir des activités de piratage étatiques.
* **Statut judiciaire :** Xu Zewei plaide non coupable et conteste toute implication, tandis que son co-accusé, Zhang Yu, est toujours en fuite.

**Vulnérabilités exploitées :**
* **Microsoft Exchange Server :** Le groupe a exploité des vulnérabilités « zero-day » critiques au sein de Microsoft Exchange Server pour déployer des *web shells* et maintenir un accès distant aux réseaux compromis. Bien que les CVE spécifiques ne soient pas mentionnées dans le texte, ces campagnes sont associées au groupe **Hafnium**, connues pour cibler les failles de type ProxyLogon (notamment **CVE-2021-26855**, **CVE-2021-26857**, **CVE-2021-26858** et **CVE-2021-27065**).

**Recommandations :**
* **Gestion des correctifs :** Appliquer systématiquement les mises à jour de sécurité critiques pour les serveurs de messagerie (Exchange) afin de limiter l'exposition aux vulnérabilités connues.
* **Surveillance réseau :** Détecter la présence de *web shells* ou d'outils d'administration distante non autorisés sur les serveurs exposés à Internet.
* **Sécurité des données sensibles :** Renforcer la segmentation réseau pour protéger les infrastructures de recherche et les données confidentielles contre les accès non autorisés.

---
[Source](https://thehackernews.com/2026/04/chinese-silk-typhoon-hacker-extradited.html){:target="_blank"}
