---
title: 'Mini Shai-Hulud Worm Compromises TanStack, Mistral AI, Guardrails AI & More Packages'
date: 2026-05-12
permalink: /posts/2026/05/12/mini-shai-hulud-worm-compromises-tanstack-mistral-ai-guardrails-ai-more-packages/
tags:
- veille-cyber
- hackernews
---
### Campagne de ver informatique « Mini Shai-Hulud » : Compromission massive de la supply chain

Le groupe de cybercriminels **TeamPCP** a orchestré une campagne sophistiquée de compromission de la chaîne d'approvisionnement logicielle, touchant plus de 170 paquets sur les registres **npm** et **PyPI**, dont des outils majeurs comme TanStack, Mistral AI, Guardrails AI et OpenSearch.

**Points clés :**
*   **Propagation automatisée :** Il s'agit d'un ver informatique capable de s'auto-propager en exploitant des jetons d'accès (GitHub/npm) et des configurations CI/CD permissives.
*   **Infrastructure de confiance détournée :** Les attaquants exploitent les mécanismes de « Trusted Publishing » et les OIDC (OpenID Connect) pour générer des jetons de publication légitimes, permettant de signer des paquets malveillants avec des attestations **SLSA Build Level 3**, trompant ainsi la vigilance des systèmes de sécurité.
*   **Mécanisme de "Dead-man's switch" :** Le malware installe un système de surveillance. Si le jeton d'accès est révoqué par le développeur, le script exécute une commande de suppression destructive (`rm -rf ~/`), transformant l'outil en destructeur de données (wiper).

**Vulnérabilités identifiées :**
*   **CVE-2026-45321** (Score CVSS : 9.6/10) : Compromission de l'écosystème TanStack via l'injection de code dans des tarballs npm.
*   **Failles opérationnelles :** Empoisonnement du cache GitHub Actions, détournement de workflows OIDC et utilisation de commits orphelins pour déclencher des exécutions malveillantes.

**Recommandations :**
*   **Isolation avant révocation :** En cas de compromission suspectée, il est impératif d'isoler et d'imager le système avant de révoquer tout jeton, sous peine de déclencher la routine destructrice du malware.
*   **Durcissement CI/CD :** Restreindre la portée des configurations de "Trusted Publishing" au niveau des fichiers de workflow et des branches protégées, plutôt que de donner une confiance étendue au dépôt entier.
*   **Analyse comportementale :** Privilégier une visibilité comportementale lors des processus d'installation (builds) plutôt que de se reposer uniquement sur les signatures ou les attestations, désormais falsifiables par détournement de processus légitimes.
*   **Audit de dépendances :** Vérifier les dépendances optionnelles et les hooks de cycle de vie (ex: `preinstall`, `prepare`) qui sont les vecteurs privilégiés pour le téléchargement de charges utiles externes (ex: via Bun ou Python).

---
[Source](https://thehackernews.com/2026/05/mini-shai-hulud-worm-compromises.html){:target="_blank"}
