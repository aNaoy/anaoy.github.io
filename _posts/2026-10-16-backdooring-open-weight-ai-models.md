---
title: 'Backdooring Open-Weight AI Models'
date: 2026-10-16
permalink: /posts/2026/10/16/backdooring-open-weight-ai-models/
tags:
- veille-cyber
- schneier
---
### La menace invisible des modèles d'IA "open-weights" modifiés

Les modèles d'intelligence artificielle dont les poids ont été modifiés — notamment via des techniques d'« abliteration » visant à contourner les filtres de sécurité — constituent des vecteurs d'attaque critiques pour la chaîne d'approvisionnement logicielle. Ces modèles peuvent héberger des portes dérobées (backdoors) indétectables par les évaluations standards, capables d'exécuter des actions malveillantes sur commande.

**Points clés :**
* **Persistance des attaques :** Les modèles empoisonnés fonctionnent normalement jusqu'à ce qu'un déclencheur spécifique (phrase, date, ou nom de client) active la charge utile malveillante.
* **Flexibilité malveillante :** En intégrant uniquement une URL vers une charge utile distante, l'attaquant peut modifier le comportement du modèle post-déploiement sans nécessiter de réentraînement.
* **Accessibilité :** La création de ces backdoors est peu coûteuse et techniquement simple, utilisant des modèles open-source populaires (Llama, Qwen) disponibles sur des plateformes comme Hugging Face.
* **Risque d'exfiltration :** Des tests ont démontré qu'un modèle compromis peut exfiltrer des identifiants de projet directement vers des outils de ligne de commande externes lors de l'activation du déclencheur.

**Vulnérabilités :**
* Absence de mécanismes de vérification de l'intégrité des poids des modèles téléchargés.
* vulnérabilité aux attaques de type « supply-chain » classiques appliquées aux composants d'IA.
* *Note : Aucun identifiant CVE spécifique n'est mentionné dans l'article, la vulnérabilité résidant dans la confiance accordée aux modèles modifiés et l'absence de traçabilité des poids.*

**Recommandations :**
* **Vérification rigoureuse :** Ne jamais utiliser de modèles modifiés ou "abliterés" sans auditer leur contenu et vérifier leur provenance.
* **Isolation :** Isoler les agents IA manipulant des données sensibles et restreindre leurs accès aux systèmes critiques.
* **Monitoring :** Mettre en place des systèmes de détection capables d'identifier des comportements anormaux ou des exfiltrations de données imprévues provenant des modèles déployés.
* **Zero Trust :** Appliquer une politique de confiance zéro à l'égard de toute dépendance logicielle ou poids de modèle tiers.

---
[Source](https://www.schneier.com/blog/archives/2026/10/backdooring-open-weight-ai-models.html){:target="_blank"}
