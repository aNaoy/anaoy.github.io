---
title: 'SAP-Related npm Packages Compromised in Credential-Stealing Supply Chain Attack'
date: 2026-04-29
permalink: /posts/2026/04/29/sap-related-npm-packages-compromised-in-credential-stealing-supply-chain-attack/
tags:
- veille-cyber
- hackernews
---
### Attaque de chaîne d'approvisionnement « Mini Shai-Hulud » ciblant l'écosystème SAP npm

Une campagne d'attaque sophistiquée, baptisée « Mini Shai-Hulud », a compromis plusieurs paquets npm liés à l'écosystème SAP et au développement d'applications cloud. Les attaquants ont injecté des scripts malveillants dans des versions légitimes pour exfiltrer des identifiants et persister au sein des environnements de développement.

#### Points clés
*   **Mode opératoire :** L'attaque utilise des scripts `preinstall` dans le fichier `package.json` pour télécharger et exécuter un binaire Bun, qui déploie ensuite le malware (`execution.js`).
*   **Cibles :** Les paquets `mbt` (v1.2.48), `@cap-js/db-service` (v2.10.1), `@cap-js/postgres` (v2.2.2) et `@cap-js/sqlite` (v2.2.2).
*   **Propagation :** Le malware utilise les tokens volés pour injecter des workflows GitHub Actions malveillants, compromettant ainsi d'autres dépôts.
*   **Innovation malveillante :** Il s'agit de l'une des premières attaques utilisant les configurations d'agents de codage IA (Claude Code et VS Code) comme vecteur de persistance via des fichiers `.claude/settings.json` et `.vscode/tasks.json`.
*   **Exfiltration :** Les données volées (clés AWS, Azure, GCP, Kubernetes, tokens GitHub/npm) sont chiffrées et envoyées vers des dépôts GitHub créés automatiquement sur les comptes des victimes.

#### Vulnérabilités exploitées
*   **Compromission de comptes :** Vol de tokens npm (statiques ou OIDC mal configurés).
*   **Mauvaise configuration CI/CD :** Les paramètres de confiance OIDC permettaient l'exécution de workflows sur des branches non protégées, facilitant la publication de paquets malveillants.
*   **Abus de configuration d'outils :** Exploitation des fonctionnalités d'exécution automatique (`runOn: folderOpen`) dans les IDE et assistants IA.

#### Recommandations
*   **Mise à jour immédiate :** Passer aux versions corrigées publiées par les mainteneurs (ex: `mbt` v1.2.49, `@cap-js/sqlite` v2.4.0/2.3.0, etc.).
*   **Audit des tokens :** Révoquer et renouveler tous les tokens npm, secrets GitHub et clés d'accès aux services cloud potentiellement exposés sur les machines de développement ou serveurs CI/CD.
*   **Renforcement CI/CD :** Restreindre les permissions OIDC aux branches principales (ex: `main`) et durcir les workflows GitHub Actions en limitant les droits `id-token: write`.
*   **Surveillance :** Inspecter les dépôts GitHub et les répertoires de développement à la recherche de fichiers suspects (`.claude/settings.json`, `.vscode/tasks.json`) ou de descriptions de dépôts mentionnant « A Mini Shai-Hulud has Appeared ».

---
[Source](https://thehackernews.com/2026/04/sap-npm-packages-compromised-by-mini.html){:target="_blank"}
