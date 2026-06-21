---
title: 'AryStinger botnet infected thousands of D-Link routers worldwide'
date: 2026-06-21
permalink: /posts/2026/06/21/arystinger-botnet-infected-thousands-of-d-link-routers-worldwide/
tags:
- veille-cyber
- bleepingcomp
---
### Le botnet AryStinger cible les routeurs D-Link obsolètes

Le botnet AryStinger a compromis plus de 4 000 routeurs, principalement les modèles D-Link DIR-850L et DIR-818LW, pour constituer un réseau distribué servant de proxy aux activités malveillantes. Ce malware transforme les équipements infectés en « exécuteurs » capables de réaliser des scans réseau, de tunneler le trafic, d'exécuter des commandes à distance, de détourner les requêtes DNS et de surveiller les données transitant sur le réseau.

**Points clés :**
*   **Architecture distribuée :** Les attaquants fractionnent des tâches massives (scans) entre plusieurs appareils infectés pour accroître l'efficacité de leurs opérations d'intrusion.
*   **Cibles géographiques :** La majorité des infections se concentre en Corée du Sud (48,5 %) et en Chine (31,8 %).
*   **Dualité du malware :** Une version en C cible les routeurs anciens, tandis qu'une version en Go, plus sophistiquée, vise les systèmes NAS avec des capacités de reconnaissance réseau avancées.

**Vulnérabilités exploitées :**
Le botnet exploite des failles connues sur du matériel en fin de vie (End-of-Life) :
*   **CVE-2013-3307**
*   **CVE-2016-5681**
*   **CVE-2025-11837**

**Recommandations de sécurité :**
*   **Remplacement matériel :** Les équipements en fin de vie doivent impérativement être remplacés par des modèles bénéficiant d'un support constructeur actif.
*   **Mise à jour :** Appliquer systématiquement les derniers correctifs de firmware disponibles.
*   **Durcissement :** Modifier les identifiants administrateurs par défaut (ne jamais conserver les mots de passe d'usine) et désactiver l'accès aux panneaux de gestion à distance.

---
[Source](https://www.bleepingcomputer.com/news/security/arystinger-botnet-infected-thousands-of-d-link-routers-worldwide/){:target="_blank"}
