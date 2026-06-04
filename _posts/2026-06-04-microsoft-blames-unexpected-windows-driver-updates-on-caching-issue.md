---
title: 'Microsoft blames unexpected Windows driver updates on caching issue'
date: 2026-06-04
permalink: /posts/2026/06/04/microsoft-blames-unexpected-windows-driver-updates-on-caching-issue/
tags:
- veille-cyber
- bleepingcomp
---
### Dysfonctionnement du cache Windows Update : déploiements de pilotes non sollicités

Microsoft a résolu un problème technique ayant entraîné l'installation automatique de pilotes sur des terminaux Windows, malgré des politiques de configuration restreignant ces mises à jour.

**Points clés :**
* **Cause technique :** Une erreur de configuration dans le service de mise en cache de Windows Update a provoqué la perte temporaire des informations d'enrôlement des appareils.
* **Impact :** Les systèmes affectés ont été considérés comme « non enrôlés », rendant inopérantes les politiques de contrôle de déploiement des administrateurs.
* **Conséquences :** Des milliers de machines ont reçu des mises à jour imprévues de pilotes et de BIOS, provoquant dans certains cas des pannes matérielles (audio/vidéo).
* **Sécurité :** Microsoft a confirmé que les pilotes installés étaient signés et approuvés, ne présentant donc pas de menace de sécurité directe.

**Vulnérabilités :**
* Aucune CVE n'a été attribuée, car il s'agit d'une défaillance opérationnelle du service cloud (Incident MO1332784) et non d'une faille logicielle exploitable.

**Recommandations :**
* **Vérification :** Les administrateurs système doivent vérifier l'état de leurs parcs informatiques pour identifier les machines ayant reçu des pilotes non autorisés.
* **Révision des déploiements :** Tester la stabilité des pilotes installés durant l'incident, particulièrement pour les composants BIOS, audio et vidéo.
* **Surveillance :** Maintenir une veille sur les tableaux de bord Microsoft Admin Center pour détecter rapidement tout écart entre les politiques définies et l'état réel des appareils gérés.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-blames-unexpected-windows-driver-updates-on-caching-issue/){:target="_blank"}
