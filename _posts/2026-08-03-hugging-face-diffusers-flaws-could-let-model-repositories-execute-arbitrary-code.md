---
title: 'Hugging Face Diffusers Flaws Could Let Model Repositories Execute Arbitrary Code'
date: 2026-08-03
permalink: /posts/2026/08/03/hugging-face-diffusers-flaws-could-let-model-repositories-execute-arbitrary-code/
tags:
- veille-cyber
- hackernews
---
### FaceHugger : Vulnérabilités critiques dans la bibliothèque Diffusers de Hugging Face

Des chercheurs ont révélé trois failles de sécurité majeures, regroupées sous le nom **FaceHugger**, affectant la bibliothèque Python *Diffusers*. Ces vulnérabilités permettent à des attaquants d'exécuter du code arbitraire sur les machines chargeant des modèles infectés, contournant ainsi le mécanisme de sécurité `trust_remote_code`. Le problème racine réside dans des conditions de type « Time-of-Check to Time-of-Use » (TOCTOU) où la vérification de sécurité n'est effectuée que lors de la phase initiale du téléchargement du modèle, permettant une injection de code ultérieure.

#### Points clés
*   **Impact :** Exécution de code arbitraire (RCE) sur les systèmes utilisant *Diffusers*, menaçant les pipelines de production et les environnements CI/CD.
*   **Cause :** Un défaut de conception dans le processus de chargement des modèles via `DiffusionPipeline.from_pretrained`, qui n'est pas une opération atomique.
*   **Vecteur :** Des dépôts Hugging Face malveillants peuvent injecter des fichiers Python personnalisés malgré le paramètre `trust_remote_code=False`.

#### Vulnérabilités identifiées
*   **CVE-2026-44827 (Score : 8.8) :** Injection de code via un pipeline crafté nommé "None.py".
*   **CVE-2026-45804 (Score : 7.5) :** Condition de concurrence (race condition) permettant de modifier la configuration entre deux appels HTTP.
*   **CVE-2026-44513 (Score : 8.8) :** Injection de code via le flux `custom_pipeline`.

#### Recommandations
*   **Mise à jour immédiate :** Passer à la version **0.38.0** ou ultérieure de la bibliothèque *Diffusers*.
*   **Sources de confiance :** Utiliser uniquement des modèles provenant de sources auditées et fiables.
*   **Audit local :** Avant de charger un modèle, inspecter manuellement les fichiers `.py` présents dans le répertoire du snapshot, notamment dans les sous-répertoires des composants (ex: `unet/`, `scheduler/`).
*   **Précautions de configuration :** Éviter de pointer `custom_pipeline` vers des dépôts tiers non vérifiés.

---
[Source](https://thehackernews.com/2026/08/hugging-face-diffusers-flaws-could-let.html){:target="_blank"}
