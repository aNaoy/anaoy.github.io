---
title: 'Over 10,000 Docker Hub images found leaking credentials, auth keys'
date: 2025-12-10
permalink: /posts/2025/12/10/over-10000-docker-hub-images-found-leaking-credentials-auth-keys/
tags:
- veille-cyber
- bleepingcomp
---
## Vulnérabilités d'Identifiants dans Docker Hub : Un Risque Majeur

Plus de 10 000 images hébergées sur Docker Hub ont révélé des informations sensibles, incluant des identifiants d'accès à des systèmes de production, des bases de données CI/CD et des clés d'accès pour des modèles d'intelligence artificielle. Ces fuites concernent environ une centaine d'organisations, dont une entreprise du classement Fortune 500 et une banque nationale.

Les chercheurs ont identifié que les secrets les plus fréquemment exposés sont des jetons d'accès pour divers modèles d'IA, tels qu'OpenAI, HuggingFace, Anthropic, Gemini et Groq, avec près de 4 000 clés trouvées. Environ 42% des images analysées contenaient au moins cinq valeurs sensibles, présentant un risque critique d'accès complet aux environnements cloud, dépôts Git, systèmes CI/CD et autres infrastructures essentielles.

Les secteurs les plus touchés incluent le développement logiciel, le marché et l'industrie, ainsi que les systèmes d'IA. Plus d'une dizaine d'entreprises financières et bancaires ont également été affectées. Les erreurs courantes identifiées sont le stockage d'identifiants et de jetons dans des fichiers .ENV, des fichiers d'application Python, des configurations YAML, et des jetons GitHub, ainsi que des informations sensibles intégrées directement dans le manifeste des images Docker. Une part importante de ces fuites provient de comptes "shadow IT", souvent utilisés à des fins personnelles ou par des contractuels, échappant ainsi aux mécanismes de surveillance d'entreprise.

Bien que près de 25% des développeurs aient corrigé la fuite dans les 48 heures, dans 75% des cas, les secrets compromis n'ont pas été révoqués, laissant la porte ouverte aux exploitations.

**Points Clés :**

*   **Volume de Fuites :** Plus de 10 000 images Docker Hub exposent des secrets.
*   **Types de Secrets :** Identifiants de production, clés CI/CD, clés LLM (IA), jetons d'accès divers.
*   **Impact :** Touche plus de 100 organisations, y compris une grande entreprise et une banque nationale.
*   **Types d'Organisations Touchées :** Principalement les secteurs du développement logiciel, marché/industrie, IA, et finance.
*   **Causes Fréquentes :** Fichiers .ENV, secrets hardcodés dans le code, manifestes d'images, comptes "shadow IT".
*   **Persistance des Fuites :** 75% des fuites ne sont pas corrigées par révocation des identifiants.

**Vulnérabilités :**

*   Absence de spécification de CVEs particulières dans l'article, mais il s'agit de mauvaises pratiques de gestion des secrets.

**Recommandations :**

*   **Pour les Développeurs :** Éviter de stocker des secrets dans les images conteneurisées, cesser l'utilisation d'identifiants statiques et à longue durée de vie, et centraliser la gestion des secrets via un gestionnaire dédié.
*   **Pour les Organisations :** Mettre en place une analyse active des secrets tout au long du cycle de développement, révoquer immédiatement les secrets exposés, et invalider les sessions anciennes.

---
[Source](https://www.bleepingcomputer.com/news/security/over-10-000-docker-hub-images-found-leaking-credentials-auth-keys/){:target="_blank"}
