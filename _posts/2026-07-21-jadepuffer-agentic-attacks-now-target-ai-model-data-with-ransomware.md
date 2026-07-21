---
title: 'JadePuffer agentic attacks now target AI model data with ransomware'
date: 2026-07-21
permalink: /posts/2026/07/21/jadepuffer-agentic-attacks-now-target-ai-model-data-with-ransomware/
tags:
- veille-cyber
- bleepingcomp
---
### Menace émergente : Le ransomware EncForge cible spécifiquement les actifs IA

L'agent autonome JadePuffer a évolué pour déployer *EncForge*, un ransomware conçu spécifiquement pour paralyser les infrastructures d'intelligence artificielle. Contrairement aux rançongiciels classiques, cet outil cible les fichiers critiques nécessaires à l'entraînement et à l'exécution des modèles.

**Points clés :**
*   **Capacité autonome :** L'agent JadePuffer est capable de résoudre les difficultés techniques en temps réel, optimisant ses scripts de déploiement en quelques minutes sans intervention humaine.
*   **Ciblage spécialisé :** Le malware crypte environ 180 extensions de fichiers liées à l'IA, notamment les poids de modèles (PyTorch, TensorFlow, SafeTensors), les bases de données vectorielles (FAISS) et les datasets d'entraînement (Parquet, Arrow).
*   **Mode opératoire :** EncForge utilise le chiffrement AES-256 (protégé par RSA-2048) en chiffrant des portions stratégiques des fichiers pour maximiser la vitesse de destruction.
*   **Impact financier :** La perte de données liées aux modèles peut entraîner des préjudices allant de 75 000 $ à 500 000 $ par unité, en raison du coût élevé de réentraînement et de réglage fin (*fine-tuning*).

**Vulnérabilité exploitée :**
*   **CVE-2025-3248 :** Vulnérabilité présente dans l'instance Langflow permettant l'accès initial, couplée à une mauvaise configuration des sockets Docker (accès root).

**Recommandations :**
*   **Mise à jour :** Installer Langflow version 1.3.0 ou supérieure pour corriger la vulnérabilité connue.
*   **Durcissement Docker :** Restreindre strictement l'accès aux sockets Docker et éviter d'exécuter les conteneurs avec des privilèges root.
*   **Contrôle d'accès :** Mettre en place des permissions de système de fichiers rigoureuses sur les répertoires contenant les poids des modèles et les datasets sensibles.

---
[Source](https://www.bleepingcomputer.com/news/security/jadepuffer-agentic-attacks-now-target-ai-model-data-with-ransomware/){:target="_blank"}
