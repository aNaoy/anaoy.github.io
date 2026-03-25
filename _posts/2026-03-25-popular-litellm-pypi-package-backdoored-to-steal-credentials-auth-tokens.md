---
title: 'Popular LiteLLM PyPI package backdoored to steal credentials, auth tokens'
date: 2026-03-25
permalink: /posts/2026/03/25/popular-litellm-pypi-package-backdoored-to-steal-credentials-auth-tokens/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de la chaîne d'approvisionnement : Le package LiteLLM infecté

Le groupe de cybercriminels « TeamPCP » a compromis le package Python populaire **LiteLLM** sur le dépôt PyPI en publiant les versions malveillantes **1.82.7** et **1.82.8**. Cette attaque par chaîne d'approvisionnement vise à exfiltrer des données sensibles et à établir une persistance durable sur les systèmes infectés.

**Points clés :**
*   **Mécanisme d'infection :** Le code malveillant est injecté via une charge utile encodée en base64 dans `proxy_server.py`. La version 1.82.8 installe un fichier `.pth` pour garantir que le script s'exécute automatiquement au démarrage de l'interpréteur Python, même si LiteLLM n'est pas utilisé directement.
*   **Objectifs :** Déploiement d'un infostealer, mouvement latéral au sein des clusters Kubernetes et installation d'une porte dérobée (backdoor) persistante de type *systemd*.
*   **Données ciblées :** Clés SSH, jetons cloud (AWS, GCP, Azure), secrets Kubernetes, fichiers `.env`, identifiants de bases de données, portefeuilles crypto et secrets CI/CD.

**Vulnérabilités :**
*   Bien qu'aucune CVE spécifique n'ait été assignée à cette compromission logicielle, l'attaque repose sur l'exploitation de la confiance accordée aux packages open-source et sur l'exécution automatique des fichiers `.pth` par Python.

**Recommandations :**
*   **Audit immédiat :** Vérifier si les versions 1.82.7 ou 1.82.8 sont installées et revenir à la version 1.82.6.
*   **Rotation des secrets :** Considérer tous les identifiants, jetons et clés présents sur les machines ayant utilisé ces versions comme compromis et procéder à une rotation immédiate.
*   **Nettoyage technique :** Rechercher des artefacts de persistance (ex: `~/.config/sysmon/sysmon.py`), des fichiers temporaires suspects (`/tmp/pglog`, `/tmp/.pg_state`) et inspecter les clusters Kubernetes pour détecter tout pod non autorisé dans `kube-system`.
*   **Surveillance réseau :** Bloquer ou surveiller les communications vers les domaines liés à l'attaquant, notamment `models.litellm[.]cloud` et `checkmarx[.]zone`.

---
[Source](https://www.bleepingcomputer.com/news/security/popular-litellm-pypi-package-compromised-in-teampcp-supply-chain-attack/){:target="_blank"}
