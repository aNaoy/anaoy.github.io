---
title: 'Hiding Capabilities in AI Models'
date: 2026-10-27
permalink: /posts/2026/10/27/hiding-capabilities-in-ai-models/
tags:
- veille-cyber
- schneier
---
### La dissimulation cryptographique de capacités dans les modèles d'IA

Des recherches récentes démontrent qu'il est possible d'insérer des capacités malveillantes complexes au sein d'un modèle d'IA sans qu'elles puissent être détectées par les audits de sécurité standards. En utilisant des techniques de chiffrement, des circuits neuronaux entiers peuvent être intégrés dans les poids du modèle hôte, restant dormants et indéchiffrables jusqu'à l'activation par un déclencheur spécifique (trigger).

**Points clés :**
*   **Dissimulation par chiffrement :** L'utilisation de "casiers numériques" permet d'encapsuler des calculs arbitraires au sein du modèle.
*   **Inviolabilité théorique :** Même avec un accès complet aux poids du modèle, les capacités cachées sont prouvées mathématiquement comme étant extrêmement difficiles à extraire ou à interpréter.
*   **Échec des méthodes d'audit :** Les techniques classiques d'évaluation (fine-tuning, analyse de gradients, entraînement adverse latent) sont inefficaces contre ces mécanismes.

**Vulnérabilités :**
*   **Absence de CVE spécifique :** Il s'agit d'une faille conceptuelle fondamentale dans l'architecture des réseaux de neurones plutôt qu'une vulnérabilité logicielle isolée. Le risque réside dans la manipulation malveillante des poids du modèle lors de la chaîne d'approvisionnement.

**Recommandations :**
*   **Mise en question des audits actuels :** Reconnaître que l'audit basé sur l'élicitation (chercher à faire "parler" le modèle) est insuffisant pour garantir l'absence de comportements cachés.
*   **Renforcement de la chaîne de confiance :** Privilégier la transparence des données d'entraînement et la sécurisation du processus de création des modèles pour empêcher l'insertion de "backdoors" cryptographiques dès la conception.
*   **Développement de nouvelles défenses :** Utiliser les modèles de preuve de concept mis à disposition par les chercheurs pour concevoir des mécanismes de détection plus robustes, capables de contrer des menaces fondées sur la cryptographie.

---
[Source](https://www.schneier.com/blog/archives/2026/10/hiding-capabilities-in-ai-models.html){:target="_blank"}
