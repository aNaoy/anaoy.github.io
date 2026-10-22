---
title: 'LiteLLM Suspects GitHub Token Leak in AI Gateway Logs Behind Malicious Package Release'
date: 2026-10-22
permalink: /posts/2026/10/22/litellm-suspects-github-token-leak-in-ai-gateway-logs-behind-malicious-package-release/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne d’approvisionnement de LiteLLM : Analyse de l'attaque

Le projet open-source **LiteLLM** a subi une compromission de sa chaîne d'approvisionnement le 21 octobre 2026, entraînant la publication de versions malveillantes (v1.107.0) sur PyPI, Docker Hub et GHCR. L'attaque a transformé ces versions en chevaux de Troie d'accès à distance (RAT), permettant l'exfiltration massive de secrets et l'exécution de code arbitraire.

#### Points clés
* **Méthode d'infection :** L'attaquant a utilisé des identifiants GitHub CLI volés pour désactiver les protections de branches et forcer la publication d'artefacts corrompus via un dépôt contrefait (*Berri-AI* au lieu de *BerriAI*).
* **Vecteur d'accès initial :** L'attaquant aurait récupéré des jetons OAuth GitHub dans les journaux d'un déploiement interne de LiteLLM exposé par erreur sur Internet.
* **Technique persistante :** L'utilisation conjointe de fichiers `.pth` et `sitecustomize.py` pour charger automatiquement des scripts malveillants au démarrage de l'interpréteur Python, une méthode inédite "dans la nature".
* **Objectif (LLMjacking) :** Les attaquants ont exploité les secrets volés (notamment des jetons AWS) pour effectuer de l'énumération de ressources et du vol de modèles d'IA.

#### Vulnérabilités identifiées
* **Fuite de jetons dans les journaux :** Les réponses des outils d'IA (ex: Claude Code) contenant des jetons OAuth étaient journalisées, rendant ces secrets accessibles en cas d'exposition du déploiement.
* **Gestion des permissions :** L'extension temporaire des privilèges de publication à plusieurs ingénieurs a élargi la surface d'attaque.
* **Absence de protection des artefacts :** Le contournement des règles de branche a permis de signer et publier des versions non vérifiées.
* *Note : Aucune CVE spécifique n'est associée à cet incident, l'attaque reposant sur l'exploitation d'identifiants légitimes et de configurations vulnérables.*

#### Recommandations
1. **Remédiation immédiate :** Supprimer la version 1.107.0 et isoler les environnements où elle a été exécutée.
2. **Rotation des secrets :** Considérer comme compromis tous les identifiants (clés API, AWS, jetons GitHub) présents sur les machines ou serveurs ayant installé la version corrompue.
3. **Audit et durcissement :**
    * Vérifier l'accessibilité publique des outils internes (logs, déploiements).
    * Restreindre strictement les permissions de publication sur les dépôts GitHub.
    * Implémenter l'immutabilité des tags Docker et la signature rigoureuse des images.
4. **Surveillance :** Rechercher la présence de fichiers suspects (`cook.pth`, `sitecustomize.py`) et bloquer toute tentative de connexion vers des domaines de C2 identifiés via des dépôts GitHub.

---
[Source](https://thehackernews.com/2026/10/litellm-suspects-github-token-leak-in.html){:target="_blank"}
