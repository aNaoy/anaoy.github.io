---
title: 'Malicious AI agents steal 600K credit cards, infect 100+ sites with skimmers'
date: 2026-09-23
permalink: /posts/2026/09/23/malicious-ai-agents-steal-600k-credit-cards-infect-100-sites-with-skimmers/
tags:
- veille-cyber
- bleepingcomp
---
### Vague d'attaques automatisées par agents IA : 600 000 cartes bancaires dérobées

Une campagne malveillante sophistiquée, active depuis juillet, utilise des frameworks d'IA open-source pour automatiser le piratage de sites e-commerce à grande échelle. Cette opération a permis le vol de plus de 600 000 données de cartes bancaires et l'infection par des "skimmers" (logiciels de vol de données de paiement) d'au moins 119 sites web, incluant de grandes entreprises.

**Points clés :**
* **Automatisation complète :** L'attaque repose sur trois outils d'IA : *Strix* (scan et vulnérabilités), *Cairn* (exploitation autonome) et *Hermes* (orchestration et prise de décision).
* **Efficacité redoutable :** L'attaquant réalise en moyenne 105 vagues d'attaques en cinq jours, avec un coût opérationnel dérisoire estimé à environ 25 $ par cible.
* **Destruction de preuves :** Les agents IA ont pour instruction de supprimer les données extraites des bases de données cibles après le vol, provoquant des perturbations opérationnelles majeures chez les victimes.
* **Méthodes d'infection :** Injection de scripts malveillants dans des fichiers JavaScript légitimes, empoisonnement de caches CDN/S3, modification de déploiements Kubernetes et utilisation de tâches planifiées (cron jobs) pour maintenir la persistance.

**Vulnérabilités :**
Bien que l'article ne mentionne pas de CVE spécifiques, les vecteurs d'attaque exploitent des failles variées selon l'architecture des cibles (Magento est nommément cité comme cible privilégiée). L'IA prioritise les entreprises utilisant des logiciels personnalisés, souvent moins bien sécurisés.

**Recommandations :**
* **Surveillance proactive :** Détecter les modifications inhabituelles sur les fichiers JavaScript critiques, les balises de checkout et les configurations de serveurs (CDN/S3/Kubernetes).
* **Gestion de la persistance :** Auditer régulièrement les tâches planifiées (cron jobs) et les processus automatisés qui pourraient restaurer des scripts malveillants après suppression.
* **Sauvegardes résilientes :** Étant donné que l'attaquant supprime les données après le vol, des sauvegardes robustes et isolées sont essentielles pour restaurer rapidement l'activité en cas d'intrusion.
* **Défense à la vitesse de la machine :** Adopter des stratégies de sécurité capables de valider et de corriger les vulnérabilités en temps réel pour contrer la vitesse d'exécution des agents autonomes.

---
[Source](https://www.bleepingcomputer.com/news/security/malicious-ai-agents-steal-600k-credit-cards-infect-100-plus-sites-with-skimmers/){:target="_blank"}
