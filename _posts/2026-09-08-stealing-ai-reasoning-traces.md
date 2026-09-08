---
title: 'Stealing AI Reasoning Traces'
date: 2026-09-08
permalink: /posts/2026/09/08/stealing-ai-reasoning-traces/
tags:
- veille-cyber
- schneier
---
### Vulnérabilité critique dans le chiffrement des chaînes de pensée (CoT) des LLM

Des chercheurs ont identifié une faille architecturale majeure concernant la gestion des traces de raisonnement (« chain-of-thought ») par les principaux fournisseurs d'IA (OpenAI, Anthropic, Google). Pour protéger leur propriété intellectuelle, ces derniers chiffrent les étapes de réflexion côté client, les renvoyant au serveur à chaque requête. 

**Points clés :**
* **Interopérabilité dangereuse :** Les blocs chiffrés sont interchangeables entre différents modèles, sessions et utilisateurs d'un même fournisseur.
* **Méthode d'attaque :** En injectant un bloc chiffré provenant d'un modèle puissant dans un modèle moins sécurisé du même écosystème, il est possible de forcer ce dernier à déchiffrer et afficher le raisonnement en texte clair.
* **Vecteurs d'attaque :**
    * **Distillation forcée :** Extraction des capacités de raisonnement propriétaire.
    * **Exfiltration de données :** Récupération de PII et d'identifiants exposés dans des logs publics.
    * **Contournement des filtres de sécurité :** Accès aux raisonnements internes même lorsque la réponse finale est censurée.
    * **Injection de prompt invisible :** Empoisonnement des agents IA via des charges utiles cachées dans les blocs chiffrés.

**Vulnérabilités :**
* Aucune CVE n'est attribuée à ce jour, car il s'agit d'une faille de conception architecturale systémique affectant plusieurs grands fournisseurs plutôt qu'un bug logiciel spécifique.

**Recommandations :**
* **Cryptographie robuste :** Implémenter des mécanismes de chiffrement liés à la session spécifique ou à l'identité de l'utilisateur pour empêcher l'interopérabilité des blocs.
* **Gestion côté serveur :** Repenser le stockage des traces de raisonnement pour éviter l'exposition client-side.
* **Hygiène des données :** Sensibiliser les développeurs au risque de partage public de logs contenant des blocs chiffrés, dont le contenu peut être rétroactivement compromis.

---
[Source](https://www.schneier.com/blog/archives/2026/09/stealing-ai-reasoning-traces.html){:target="_blank"}
