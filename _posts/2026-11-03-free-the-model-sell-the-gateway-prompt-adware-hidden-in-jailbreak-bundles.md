---
title: 'Free the Model, Sell the Gateway: Prompt Adware hidden in Jailbreak Bundles'
date: 2026-11-03
permalink: /posts/2026/11/03/free-the-model-sell-the-gateway-prompt-adware-hidden-in-jailbreak-bundles/
tags:
- veille-cyber
- zerodaysfans
---
### Menace émergente : le "Prompt Adware" dans les kits de Jailbreak

Le bundle de jailbreak nommé **Haiou** (pour OpenAI Codex) illustre une nouvelle menace : le **"Prompt Adware"**. Ce type de logiciel ne repose pas sur des exécutables malveillants classiques, mais modifie durablement les instructions système d'un agent IA pour insérer des publicités et des incitations commerciales, tout en contournant les garde-fous de sécurité du modèle.

#### Points clés
*   **Fonctionnement :** Le bundle Haiou utilise des techniques de *prompt injection* (jeu de rôle, suppression de refus, *pretexting*) pour permettre à l'IA d'effectuer des tâches offensives (pentest, reverse engineering, cracking de logiciels).
*   **Adware par le langage :** Le package insère des instructions persistantes dans les fichiers de configuration de l'agent. Lorsqu'un utilisateur active l'IA via certains mots-clés, celle-ci répond automatiquement en faisant la promotion d'une passerelle LLM tierce (service de relais d'API).
*   **Dual-usage :** Bien que l'outil ne soit pas nativement malveillant, il a été identifié au sein de serveurs utilisés par des cybercriminels (aux côtés de Cobalt Strike, VulnClaw et Ladon), confirmant l'adoption croissante de ces outils par les acteurs de la menace pour automatiser leurs opérations.
*   **Persistance et opacité :** Le bundle utilise des signatures (Ed25519) et des fichiers chiffrés (AES-256-GCM) pour dissimuler ses prompts aux outils d'analyse automatique et éviter la détection par le fournisseur de l'IA.

#### Vulnérabilités
*   **Risque de Supply Chain :** L'utilisation de passerelles LLM (*LLM Gateways*) opaques constitue un vecteur d'attaque critique. Ces services peuvent espionner les données des utilisateurs, intercepter des secrets (clés d'API, tokens) ou injecter des outils d'exécution de code à distance.
*   **Manipulation comportementale :** Au-delà de la publicité, ce mécanisme de persistance peut être utilisé pour biaiser subtilement les conseils techniques, orienter les recommandations ou influencer les décisions de l'utilisateur à son insu.

#### Recommandations
*   **Méfiance vis-à-vis des bundles tiers :** Éviter d'installer des packages d'amélioration ("enhancement packages") ou des jailbreaks provenant de dépôts GitHub non vérifiés, surtout lorsqu'ils incluent des fichiers chiffrés ou opaques.
*   **Audit des configurations d'agents :** Vérifier régulièrement les fichiers de configuration globale (prompts systèmes, "Skills", instructions de comportement) des agents IA pour détecter toute modification non autorisée ou insertion de texte suspect.
*   **Usage de passerelles sécurisées :** Prioriser l'utilisation des API officielles des fournisseurs de modèles plutôt que des passerelles tierces non auditées, afin de prévenir le vol de données ou l'injection de code malveillant.
*   **Surveillance des logs :** Être attentif aux réponses récurrentes de l'IA qui semblent dévier de leur rôle technique ou promouvoir des services tiers, ce qui pourrait indiquer une compromission de la couche d'instructions système.

---
[Source](https://research.checkpoint.com/2026/free-the-model-sell-the-gateway-prompt-adware-hidden-in-jailbreak-bundles/){:target="_blank"}
