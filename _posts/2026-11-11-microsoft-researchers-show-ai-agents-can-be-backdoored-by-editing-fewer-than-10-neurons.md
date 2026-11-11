---
title: 'Microsoft Researchers Show AI Agents Can Be Backdoored by Editing Fewer Than 10 Neurons'
date: 2026-11-11
permalink: /posts/2026/11/11/microsoft-researchers-show-ai-agents-can-be-backdoored-by-editing-fewer-than-10-neurons/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité des agents IA : la menace « Lazarus »

Des chercheurs de Microsoft ont démontré une nouvelle technique baptisée **Lazarus**, permettant d'insérer une porte dérobée (backdoor) dans un modèle d'IA en modifiant moins de 10 neurones, sans nécessiter de réentraînement complet.

**Points clés :**
* **Fonctionnement :** L'attaque cible des neurones rarement utilisés pour déclencher l'exécution d'une commande malveillante lorsqu'une chaîne de caractères spécifique (déclencheur) est détectée dans la requête ou la sortie d'un outil.
* **Discrétion :** Les performances générales du modèle restent quasi inchangées, rendant la modification invisible lors des tests de fonctionnement standards.
* **Vecteur d'attaque :** Toute entité capable de modifier le fichier des poids (checkpoint) d'un modèle peut implanter ce backdoor (initiés, compromission de pipeline de build, ou téléchargement de modèles sur des dépôts publics).
* **Impact :** La gravité dépend des permissions accordées à l'agent IA. Un agent exécutant du code avec des droits élevés (ex: root) peut être forcé d'exécuter des scripts arbitraires à distance.

**Vulnérabilités :**
* Il n'existe pas de CVE spécifique, car il s'agit d'une vulnérabilité structurelle liée à la manipulation des poids des réseaux de neurones. Le risque concerne la confiance accordée aux modèles "open-weights" téléchargés depuis des sources non vérifiées.

**Recommandations de sécurité :**
* **Audit des poids :** Comparer systématiquement le hash des checkpoints avec ceux des éditeurs officiels.
* **Gestion des sources :** Utiliser des registres privés et bloquer les accès directs aux hubs de modèles publics.
* **Isolation :** Exécuter le code généré par les agents dans des environnements isolés (sandboxes) avec des accès réseau restreints.
* **Privilèges minimaux :** Appliquer le principe du moindre privilège aux agents et exiger une validation humaine pour toute action critique ou sortante.
* **Détection comportementale :** Combiner l'analyse des poids avec des outils de scan comportemental pour identifier les comportements anormaux des modèles.

---
[Source](https://thehackernews.com/2026/11/microsoft-researchers-show-ai-agents.html){:target="_blank"}
