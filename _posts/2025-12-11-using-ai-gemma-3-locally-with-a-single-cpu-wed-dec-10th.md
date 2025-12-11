---
title: 'Using AI Gemma 3 Locally with a Single CPU , (Wed, Dec 10th)'
date: 2025-12-11
permalink: /posts/2025/12/11/using-ai-gemma-3-locally-with-a-single-cpu-wed-dec-10th/
tags:
- veille-cyber
- sans-isc
---
**Installation Locale de Gemma 3 sur CPU avec Interface Web**

Il est possible d'exécuter des modèles d'intelligence artificielle générative de Google Gemma 3 directement sur un ordinateur personnel, y compris sur un processeur (CPU) sans nécessiter de matériel dédié coûteux. L'article détaille la mise en place de Gemma 3 sur un mini-ordinateur équipé d'un processeur AMD Ryzen. L'installation passe par l'utilisation d'Ollama pour gérer les modèles et d'Open WebUI pour fournir une interface graphique accessible via un navigateur web.

**Points Clés :**

*   Gemma 3 est une famille de modèles d'IA générative polyvalents (question/réponse, résumé, raisonnement).
*   Les modèles Gemma 3 existent en différentes tailles (270M, 1B, 4B, 12B, 27B), nécessitant des quantités de RAM variables.
*   Il est possible de commencer avec des modèles plus petits pour tester avant de passer à des modèles plus grands.
*   Pour un fonctionnement optimal sur certains systèmes, notamment sous Proxmox 9 avec des conteneurs LXC, des ajustements de configuration concernant AppArmor sont nécessaires.
*   L'interface Open WebUI permet une interaction conviviale avec les modèles Gemma 3.
*   Gemma 3 peut traiter de grands volumes de texte (contexte 128K), intégrer des images et prend en charge plusieurs langues.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans cet article. L'accent est mis sur la configuration et l'utilisation locale des modèles.

**Recommandations :**

*   Vérifier les prérequis en RAM pour choisir le modèle Gemma 3 approprié.
*   Commencer avec des modèles plus petits (ex: 4B) pour des tests initiaux.
*   Pour les utilisateurs de Proxmox 9 avec des conteneurs LXC, modifier les fichiers de configuration de LXC pour désactiver AppArmor si nécessaire afin d'assurer le bon fonctionnement.
*   Installer le logiciel `admgpu` si le CPU possède des capacités d'IA intégrées (comme le Ryzen 7 mentionné).
*   Utiliser Open WebUI pour une interface utilisateur graphique facilitant l'interaction.

---
[Source](https://isc.sans.edu/diary/rss/32556){:target="_blank"}
