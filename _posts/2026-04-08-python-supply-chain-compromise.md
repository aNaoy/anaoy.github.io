---
title: 'Python Supply-Chain Compromise'
date: 2026-04-08
permalink: /posts/2026/04/08/python-supply-chain-compromise/
tags:
- veille-cyber
- schneier
---
### Compromission de la chaîne d'approvisionnement Python : Le cas LiteLLM

Une compromission critique a été identifiée dans la version 1.82.8 du package Python **LiteLLM** sur le dépôt PyPI. Cette attaque de la chaîne d'approvisionnement permet une exécution de code arbitraire persistante sur les systèmes des utilisateurs.

**Points clés :**
*   **Mécanisme d'infection :** L'archive contient un fichier malveillant nommé `litellm_init.pth`.
*   **Exécution automatique :** Le fichier `.pth` est chargé par l'interpréteur Python dès son démarrage, ce qui déclenche le code malveillant sans même que le module LiteLLM ne soit importé ou utilisé explicitement.

**Vulnérabilités :**
*   **CVE :** Aucune CVE n'a été officiellement attribuée à ce jour pour cet incident spécifique.
*   **Vecteur d'attaque :** Utilisation détournée de la fonctionnalité des fichiers `.pth` de Python, qui permet l'exécution automatique de code lors de l'initialisation du site.

**Recommandations :**
*   **Vérification immédiate :** Supprimer la version 1.82.8 de LiteLLM de tous les environnements et auditer les systèmes pour détecter la présence de fichiers `.pth` suspects.
*   **Renforcement de la sécurité de la supply-chain :** Adopter des mesures de contrôle rigoureuses, notamment :
    *   La mise en œuvre de **SBOM** (Software Bill of Materials) pour tracer les dépendances.
    *   L'utilisation de **SLSA** (Supply chain Levels for Software Artifacts) pour garantir l'intégrité des artefacts.
    *   L'adoption de **SigStore** pour la signature numérique des packages afin d'assurer leur authenticité.

---
[Source](https://www.schneier.com/blog/archives/2026/04/python-supply-chain-compromise.html){:target="_blank"}
