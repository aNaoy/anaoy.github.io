---
title: 'New ENCFORGE Ransomware Targets AI Model Files in Langflow RCE Attack'
date: 2026-07-21
permalink: /posts/2026/07/21/new-encforge-ransomware-targets-ai-model-files-in-langflow-rce-attack/
tags:
- veille-cyber
- hackernews
---
### ENCFORGE : Le ransomware ciblant spécifiquement les infrastructures d'IA

Le groupe d'attaquants derrière l'agent JADEPUFFER a déployé un nouveau ransomware compilé en Go, baptisé **ENCFORGE**, spécifiquement conçu pour chiffrer les actifs critiques des environnements d'IA (poids de modèles, jeux de données, index vectoriels).

#### Points clés
*   **Vecteur d'attaque :** Utilisation d'une vulnérabilité RCE (exécution de code à distance) dans Langflow pour obtenir un accès initial, suivie d'une élévation de privilèges via une évasion de conteneur Docker.
*   **Mode opératoire :** L'attaquant manipule l'API Docker pour monter le système de fichiers racine de l'hôte et exécuter le payload avec des privilèges élevés (`nsenter`).
*   **Ciblage :** Le malware identifie et chiffre environ 180 types de fichiers spécifiques aux workflows IA (PyTorch, TensorFlow, Hugging Face, GGUF, etc.) via l'algorithme AES-256-CTR.
*   **Absence d'exfiltration :** Le ransomware se concentre uniquement sur la destruction par chiffrement et ne possède aucune fonction d'exfiltration de données, utilisant la menace de perte de modèles comme levier d'extorsion.

#### Vulnérabilités exploitées
*   **CVE-2025-3248 :** RCE critique dans Langflow (score CVSS 9.8).
*   **Vulnérabilités associées (KEV) :** L'article mentionne également **CVE-2026-33017** et **CVE-2026-55255** comme des failles Langflow actives nécessitant une mise à jour immédiate.

#### Recommandations de sécurité
*   **Mise à jour :** Passer impérativement à Langflow version 1.9.1 ou supérieure.
*   **Gestion des accès :** Révoquer et renouveler toutes les clés d'API, secrets de base de données et identifiants cloud potentiellement compromis par l'instance Langflow.
*   **Sécurisation Docker :** Supprimer l'accès au socket Docker (`/var/run/docker.sock`) des conteneurs. Si indispensable, utiliser un proxy restreint et interdire les conteneurs privilégiés ou avec accès au namespace de l'hôte (`PidMode: host`).
*   **Protection des données :** Stocker les poids de modèles, index et datasets dans des sauvegardes immuables ou hors ligne.
*   **Détection :** Monitorer la création de conteneurs privilégiés, l'utilisation de `nsenter` depuis des conteneurs, et la création massive de fichiers `.locked`.

---
[Source](https://thehackernews.com/2026/07/new-encforge-ransomware-targets-ai.html){:target="_blank"}
