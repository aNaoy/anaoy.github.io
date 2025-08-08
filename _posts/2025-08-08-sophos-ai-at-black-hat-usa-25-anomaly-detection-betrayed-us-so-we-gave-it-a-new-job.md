---
title: 'Sophos AI at Black Hat USA ’25: Anomaly detection betrayed us, so we gave it a new job'
date: 2025-08-08
permalink: /posts/2025/08/08/sophos-ai-at-black-hat-usa-25-anomaly-detection-betrayed-us-so-we-gave-it-a-new-job/
tags:
- veille-cyber
- sophos
---
## Renouveler la détection d'anomalies pour la classification des lignes de commande

Une nouvelle approche exploite les capacités des grands modèles de langage (LLM) pour enrichir les données d'entraînement des systèmes de classification de lignes de commande, réduisant ainsi les faux positifs. Au lieu de chercher directement les comportements malveillants, cette méthode utilise la détection d'anomalies pour identifier une diversité de commandes "bénignes" inhabituelles.

**Points clés :**

*   La détection d'anomalies directe pour identifier les commandes malveillantes génère souvent trop de faux positifs, la rendant inefficace.
*   Une nouvelle méthode combine la détection d'anomalies avec des LLM pour étiqueter précisément les commandes.
*   L'objectif est de découvrir une grande variété de commandes bénignes, même complexes ou rares, pour entraîner des classificateurs plus robustes.
*   Cette stratégie permet d'utiliser des données existantes abondantes sans dépendre de la difficulté à trouver des exemples rares de commandes malveillantes.
*   L'approche a montré une amélioration significative des performances des modèles de classification, mesurée par l'aire sous la courbe (AUC).
*   La méthode est adaptable et peut être intégrée dans des pipelines de production existants.

**Vulnérabilités et recommandations :**

Bien que l'article ne détaille pas de CVE spécifiques, il adresse la vulnérabilité inhérente aux systèmes de détection d'anomalies classiques qui souffrent de taux élevés de faux positifs.

*   **Problème :** Les classificateurs ont tendance à mal interpréter des commandes bénignes complexes ou rares comme malveillantes, entraînant des faux positifs. La mise à l'échelle des données d'entraînement avec des exemples bénins classiques ne parvient pas à couvrir cette "longue traîne" de variations.
*   **Recommandation :** Utiliser la détection d'anomalies pour identifier et étiqueter automatiquement, à l'aide de LLM, un ensemble diversifié de commandes bénignes. L'intégration de ces données bénignes enrichies dans l'entraînement des classificateurs améliorera leur précision et réduira les faux positifs. La sélection d'un modèle LLM performant pour l'étiquetage (par exemple, OpenAI's o3-mini) et l'utilisation d'embeddings sémantiques (comme Jina Embeddings V2) pour le traitement des données sont recommandées pour une efficacité accrue. La mise en place d'une étape de déduplication des anomalies détectées est également cruciale pour éviter les redondances.

---
[Source](https://news.sophos.com/en-us/2025/08/07/sophos-ai-at-black-hat-usa-25-anomaly-detection-betrayed-us-so-we-gave-it-a-new-job/){:target="_blank"}
