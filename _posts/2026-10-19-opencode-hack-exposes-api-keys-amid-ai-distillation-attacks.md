---
title: 'OpenCode hack exposes API keys amid AI distillation attacks'
date: 2026-10-19
permalink: /posts/2026/10/19/opencode-hack-exposes-api-keys-amid-ai-distillation-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Cyberattaque par distillation de modèle chez OpenCode

Le projet d'IA open-source OpenCode a été victime d'une attaque par « distillation » massive ayant conduit à l'exfiltration de clés API d'utilisateurs connectés à des services tiers (Google Cloud, OpenAI, Anthropic). Cette violation a permis aux attaquants de détourner des ressources cloud, entraînant des frais non autorisés pouvant atteindre 1 700 $ par utilisateur et la suspension de certains comptes Google Cloud.

**Points clés :**
* **Nature de l'attaque :** Utilisation détournée de la distillation de modèle (entraînement de modèles plus petits via des requêtes massives) pour exfiltrer des identifiants API stockés.
* **Impact :** 1,4 % des utilisateurs de la console OpenCode ont été touchés à partir du 17 octobre 2026.
* **Réponse incidente :** OpenCode a stabilisé son système en déployant le modèle de cybersécurité « Daybreak » d'OpenAI pour bloquer les requêtes malveillantes.
* **Conséquences opérationnelles :** Frais financiers frauduleux importants et blocage de projets par les fournisseurs de services cloud.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée à cet incident, la faille reposant sur l'exploitation à grande échelle d'agents IA pour contourner les protections et extraire des secrets utilisateur stockés dans la console.

**Recommandations :**
* **Révoquer les clés :** Les utilisateurs concernés doivent immédiatement révoquer et régénérer leurs clés API auprès de leurs fournisseurs (OpenAI, Google, Anthropic).
* **Surveillance financière :** Contrôler étroitement les factures et les alertes de consommation sur les plateformes Cloud.
* **Sécurisation des accès :** Appliquer le principe du moindre privilège aux clés API et, dans la mesure du possible, utiliser des mécanismes d'authentification à durée limitée ou des coffres-forts de secrets (secrets management) plutôt que de stocker les clés en clair dans des consoles d'outils tiers.
* **Suivi des notifications :** Les utilisateurs n'ayant pas reçu d'e-mail de la part d'OpenCode ne sont, selon l'éditeur, pas impactés.

---
[Source](https://www.bleepingcomputer.com/news/security/opencode-hack-exposes-api-keys-amid-ai-distillation-attacks/){:target="_blank"}
