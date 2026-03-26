---
title: 'An AI gateway designed to steal your data'
date: 2026-03-26
permalink: /posts/2026/03/26/an-ai-gateway-designed-to-steal-your-data/
tags:
- veille-cyber
- securelist
---
### Attaque par empoisonnement de la chaîne d'approvisionnement : Le cas LiteLLM

En mars 2026, des attaquants ont compromis la bibliothèque Python populaire **LiteLLM** en publiant des versions malveillantes (1.82.7 et 1.82.8) sur le dépôt PyPI. Cette attaque de type "supply chain" visait à exfiltrer des données sensibles et à établir une persistance durable au sein des infrastructures cloud et Kubernetes des développeurs.

#### Points clés
*   **Vecteur d'attaque :** Injection de code malveillant dans des versions légitimes de bibliothèques open-source via la compromission de comptes.
*   **Méthodologie :** Utilisation de scripts encodés en Base64, exécution via `proxy_server.py` ou des fichiers `.pth` pour une persistance au démarrage de l'interpréteur.
*   **Cibles :** Données de configuration (AWS, Kubernetes, bases de données), clés SSH, jetons d'accès cloud (via l'IMDS AWS), portefeuilles crypto et outils de communication (Slack/Discord).
*   **Extension :** L'attaque s'est étendue à des extensions VSX (Checkmarx) malveillantes, ciblant les environnements de développement pour voler des secrets locaux.
*   **Persistance :** Installation d'un service système (`sysmon.py`) et, dans Kubernetes, création de pods privilégiés pour s'échapper du conteneur et atteindre le niveau "nœud".

#### Vulnérabilités exploitées
*   **Supply Chain Attack :** Confiance aveugle dans les packages tiers des dépôts publics (PyPI, OpenVSX).
*   **Escalade de privilèges Kubernetes :** Exploitation du `securityContext.privileged=true` et `hostPath` pour briser l'isolation des conteneurs.
*   **Accès aux métadonnées cloud :** Utilisation des points de terminaison non sécurisés (169.254.169.254) pour exfiltrer des credentials IAM temporaires.
*(Note : Aucune CVE spécifique n'est associée à ces manipulations, car il s'agit d'une compromission de code source volontaire par des tiers malveillants.)*

#### Recommandations
*   **Audit et nettoyage :** Supprimer les versions compromises de LiteLLM, vider le cache des modules et effectuer un inventaire complet des dépendances.
*   **Rotation des secrets :** Renouveler impérativement tous les jetons API, clés SSH, variables d'environnement et credentials AWS/Cloud compromis.
*   **Détection :** Rechercher la présence du fichier `~/.config/sysmon/sysmon.py` et auditer les clusters Kubernetes pour identifier des pods suspects ou privilégiés.
*   **Durcissement :** Utiliser des solutions de surveillance des composants open-source et des outils de protection EDR/XDR pour détecter les comportements anormaux en temps réel au sein du cycle de développement.

---
[Source](https://securelist.com/litellm-supply-chain-attack/119257/){:target="_blank"}
