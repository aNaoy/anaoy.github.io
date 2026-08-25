---
title: 'A Malicious Webpage Could Poison Your Local AI Model Behind NVIDIA NemoClaw'
date: 2026-08-25
permalink: /posts/2026/08/25/a-malicious-webpage-could-poison-your-local-ai-model-behind-nvidia-nemoclaw/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité d'empoisonnement de modèles IA via NVIDIA NemoClaw

Des chercheurs d'Oasis Security ont découvert une faille dans la pile NVIDIA NemoClaw permettant à un site web malveillant de prendre le contrôle d'une instance locale d'Ollama. En exploitant une configuration réseau permissive, un attaquant peut injecter des instructions persistantes directement dans le modèle d'IA via le "chat template", compromettant ainsi toutes les interactions futures de l'agent.

**Points clés :**
* **Vecteur d'attaque :** Utilisation d'une technique de rebinding DNS pour contourner les protections CORS et accéder à l'API Ollama (port 11434) sans authentification.
* **Cause racine :** NemoClaw configure Ollama avec `OLLAMA_HOST=0.0.0.0`, ce qui désactive automatiquement la validation des en-têtes "Host" d'Ollama, rendant le service vulnérable aux requêtes provenant du navigateur.
* **Persistance :** L'injection modifie le modèle au niveau local ; les instructions malveillantes deviennent invisibles pour l'utilisateur et persistent lors des conversations ultérieures.
* **Statut de la correction :** Le problème est corrigé sur macOS et Linux (v0.0.35+). Les versions Windows et WSL demeurent exposées ou nécessitent des configurations spécifiques.

**Vulnérabilités associées :**
* **CVE-2024-28224 :** Faille de rebinding DNS sur Ollama (contexte historique). La faille actuelle dans NemoClaw résulte de la désactivation par conception des protections contre ce type d'attaque lors d'une liaison sur `0.0.0.0`.

**Recommandations :**
* **Mise à jour :** Installer les dernières versions de NemoClaw sur les systèmes compatibles.
* **Configuration sécurisée :** S'assurer que le service Ollama est lié uniquement à l'interface de bouclage (`127.0.0.1`) et non à `0.0.0.0`.
* **Vigilance Windows :** Sur Windows/WSL, où le correctif est limité, éviter de naviguer sur des sites web non fiables pendant l'exécution d'un agent IA, et restreindre l'accès réseau au port 11434 par le pare-feu local.
* **Intégrité :** Implémenter des contrôles d'intégrité sur les modèles et les templates de chat pour détecter toute modification non autorisée.

---
[Source](https://thehackernews.com/2026/08/a-malicious-webpage-could-poison-your.html){:target="_blank"}
