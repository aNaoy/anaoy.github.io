---
title: 'Max-severity flaw in ChromaDB for AI apps allows server hijacking'
date: 2026-05-20
permalink: /posts/2026/05/20/max-severity-flaw-in-chromadb-for-ai-apps-allows-server-hijacking/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique dans ChromaDB : exécution de code à distance

Une faille de sécurité majeure, identifiée dans la version Python (FastAPI) de la base de données vectorielle open-source ChromaDB, permet à des attaquants non authentifiés d'exécuter du code arbitraire sur les serveurs exposés.

**Points clés :**
*   **Vulnérabilité :** CVE-2026-45829.
*   **Mécanisme :** Le contrôle d'authentification intervient trop tard dans le processus de traitement des requêtes. Un attaquant peut forcer le chargement et l'exécution d'un modèle malveillant (via Hugging Face) avant que le serveur ne rejette la requête.
*   **Impact :** Risque d'exécution de code arbitraire (RCE) avec une sévérité maximale. Environ 73 % des instances exposées sur Internet seraient vulnérables.
*   **Statut :** La faille a été introduite dans la version 1.0.0 et persiste jusqu'à la version 1.5.8. L'efficacité du correctif dans la version 1.5.9 reste incertaine, les développeurs n'ayant pas communiqué sur le sujet.

**Recommandations :**
*   **Restriction réseau :** Éviter d'exposer publiquement le serveur API Python et restreindre l'accès au port de ChromaDB.
*   **Migration :** Privilégier l'utilisation du front-end en Rust, qui n'est pas affecté par cette vulnérabilité.
*   **Sécurisation ML :** Scanner systématiquement les modèles d'apprentissage automatique avant leur exécution, car le chargement de modèles publics avec l'option `trust_remote_code` constitue un vecteur d'exécution de code non fiable.

---
[Source](https://www.bleepingcomputer.com/news/security/max-severity-flaw-in-chromadb-for-ai-apps-allows-server-hijacking/){:target="_blank"}
