---
title: 'Self-Propagating Supply Chain Worm Hijacks npm Packages to Steal Developer Tokens'
date: 2026-04-22
permalink: /posts/2026/04/22/self-propagating-supply-chain-worm-hijacks-npm-packages-to-steal-developer-tokens/
tags:
- veille-cyber
- hackernews
---
### CanisterSprawl : Attaque par ver dans la chaîne d'approvisionnement logicielle

Une campagne de cybersécurité sophistiquée, baptisée **CanisterSprawl**, cible activement l'écosystème npm via des paquets compromis. Ce ver informatique est capable de s'auto-propager en exploitant les jetons d'authentification volés aux développeurs pour publier de nouvelles versions malveillantes de paquets légitimes.

**Points clés :**
*   **Mode opératoire :** Le code malveillant est déclenché lors de l'installation du paquet via un script `postinstall`. Il exfiltre une vaste gamme de secrets (clés SSH, identifiants cloud, jetons npm, fichiers `.env`, historiques shell, etc.) vers des serveurs distants.
*   **Auto-propagation :** Le malware ne se contente pas de voler des données ; il utilise les jetons npm dérobés pour compromettre davantage de projets et possède des capacités de propagation similaire pour l'écosystème **PyPI**.
*   **Infrastructure résiliente :** Pour échapper aux démantèlements, l'attaquant utilise des *canisters* ICP (Internet Computer Protocol) et des webhooks pour l'exfiltration des données.
*   **Multiplication des menaces :** D'autres campagnes utilisant des techniques similaires (exfiltration via des proxys LLM, usurpation d'identité comme Asurion, ou exploitation du workflow GitHub `pull_request_target`) confirment une tendance croissante aux attaques automatisées ciblant les outils de développement et le CI/CD.

**Vulnérabilités :**
L'attaque repose sur l'exploitation des failles de confiance inhérentes aux scripts d'installation automatique (`postinstall`) dans les gestionnaires de paquets et sur l'exposition des secrets dans les environnements de développement. Aucune CVE unique n'est associée, car il s'agit d'une exploitation détournée de fonctionnalités légitimes de la chaîne d'outils.

**Recommandations :**
*   **Audit des dépendances :** Surveiller les versions des paquets installés, particulièrement celles listées comme compromises (ex: `@automagik/genie`, `pgserve`, etc.).
*   **Sécurisation des secrets :** Ne jamais stocker de jetons d'API, clés SSH ou identifiants cloud en clair dans les répertoires de développement (`.env`, `.npmrc`, `.git-credentials`). Utiliser des coffres-forts numériques (Vault, gestionnaires de secrets cloud).
*   **Gestion des accès CI/CD :** Appliquer le principe du moindre privilège aux flux de travail (workflows) GitHub, notamment en évitant l'usage du déclencheur `pull_request_target` sur des dépôts sensibles sans approbation manuelle stricte.
*   **Hygiène logicielle :** Désactiver l'exécution automatique de scripts lors de l'installation de dépendances si les outils de gestion de paquets le permettent, et privilégier l'utilisation de fichiers de verrouillage (lockfiles) pour garantir l'intégrité des versions installées.

---
[Source](https://thehackernews.com/2026/04/self-propagating-supply-chain-worm.html){:target="_blank"}
