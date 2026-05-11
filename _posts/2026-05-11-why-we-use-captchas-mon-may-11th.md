---
title: 'Why we use CAPTCHAs, (Mon, May 11th)'
date: 2026-05-11
permalink: /posts/2026/05/11/why-we-use-captchas-mon-may-11th/
tags:
- veille-cyber
- sans-isc
---
### L'efficacité des CAPTCHA face à l'automatisation

L'intégration de solutions de filtrage comme Cloudflare Turnstile permet de quantifier précisément l'ampleur du trafic automatisé sur un site web. Selon une analyse menée sur plusieurs mois, 99,7 % des requêtes interceptées provenaient de bots, confirmant leur rôle crucial dans la préservation des ressources serveurs.

**Points clés :**
* **Massivité des bots :** L'écrasante majorité du trafic analysé (environ 300 requêtes) est générée par des robots, incluant des scanners issus de services cloud et de réseaux sociaux.
* **Équilibre UX/Sécurité :** Le choix de Turnstile repose sur le respect de la vie privée, une faible friction pour l'utilisateur final et une intégration simplifiée via CDN.
* **Dissuasion :** L'objectif d'un CAPTCHA n'est pas l'impossibilité technique absolue de contournement, mais de rendre la tâche suffisamment coûteuse ou complexe pour décourager les attaquants.

**Vulnérabilités :**
* L'article ne mentionne pas de CVE spécifique, mais souligne une faille logique courante : la possibilité pour des utilisateurs réels de soumettre des formulaires avant la validation complète du test CAPTCHA.

**Recommandations :**
* **Validation dynamique :** Désactiver les boutons de soumission (via JavaScript) tant que le test CAPTCHA n'est pas validé par le système.
* **Surveillance du trafic :** Analyser les origines suspectes (IP fixes, fournisseurs cloud, réseaux de bots) pour affiner les règles de filtrage.
* **Sélection d'outils :** Privilégier des solutions modernes qui minimisent l'impact sur l'expérience utilisateur tout en garantissant une meilleure conformité en matière de confidentialité.

---
[Source](https://isc.sans.edu/diary/rss/32974){:target="_blank"}
