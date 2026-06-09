---
title: 'Researchers Build Self-Replicating AI Worm That Operates Entirely on Local, Open-Weight Models'
date: 2026-06-09
permalink: /posts/2026/06/09/researchers-build-self-replicating-ai-worm-that-operates-entirely-on-local-open-weight-models/
tags:
- veille-cyber
- hackernews
---
### Émergence d'un ver informatique autonome piloté par IA

Des chercheurs de l'Université de Toronto ont conçu un ver informatique exploitant des modèles de langage (LLM) en accès libre, capables de mener des attaques autonomes sans intervention humaine. Contrairement aux malwares traditionnels, ce programme génère ses propres stratégies d'attaque en temps réel, s'adapte à chaque cible rencontrée et s'auto-réplique au sein d'un réseau, sans dépendre de services d'IA externes ou d'API.

**Points clés :**
* **Fonctionnement :** Le ver utilise la puissance de calcul (GPU) des machines infectées pour exécuter des modèles de raisonnement locaux, permettant d'identifier des vulnérabilités et de créer des exploits dynamiques.
* **Autonomie :** Lors des tests, le ver a infecté 62 % d'un réseau isolé en sept jours, sans connaissance préalable de la topologie.
* **Adaptabilité :** Le malware est capable d'analyser des avis de sécurité publics (CVE) publiés après son entraînement pour élaborer des exploits contre des failles "zéro-day" ou récemment divulguées.
* **Absence de "Kill Switch" :** L'utilisation de modèles en open-weight supprime toute dépendance envers un fournisseur, rendant inefficaces les mécanismes de blocage habituels (révocation d'API, limites de taux).

**Vulnérabilités exploitées (exemples notables) :**
* **CVE-2026-39987 :** Exécution de code à distance (RCE) dans Marimo (CVSS 9.3).
* **CVE-2026-31431 (CopyFail) :** Élévation de privilèges dans le noyau Linux.
* **CVE-2026-43284 / CVE-2026-43500 (DirtyFrag) :** Problèmes d'élévation de privilèges locaux sous Linux.

**Recommandations pour la défense :**
* **Segmentation réseau :** Isoler strictement les machines dotées de capacités GPU, car elles servent de nœuds de calcul pour le raisonnement du ver.
* **Gestion des patchs :** Réduire drastiquement le temps entre la publication d'un avis de sécurité (CVE) et son application, les attaquants automatisant désormais l'exploitation des vulnérabilités connues en quelques heures.
* **Rotation des accès :** Appliquer une rotation systématique des identifiants dès qu'une compromission est suspectée, le ver exploitant activement la réutilisation des credentials.
* **Détection comportementale :** Surveiller les signes anormaux comme des clusters d'inférences LLM sur des terminaux non prévus, l'injection automatisée de clés SSH et une activité réseau inhabituelle.

---
[Source](https://thehackernews.com/2026/06/researchers-build-self-replicating-ai.html){:target="_blank"}
