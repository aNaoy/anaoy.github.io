---
title: 'TeamPCP Supply Chain Campaign: Activity Through 2026-05-24, (Mon, May 25th)'
date: 2026-05-25
permalink: /posts/2026/05/25/teampcp-supply-chain-campaign-activity-through-2026-05-24-mon-may-25th/
tags:
- veille-cyber
- sans-isc
---
### Campagne de supply chain "TeamPCP" : Escalade et compromissions massives

La campagne "TeamPCP" a franchi un cap critique en ciblant simultanément les écosystèmes VS Code, PyPI et npm. En une semaine, le groupe a compromis l'infrastructure interne de GitHub, empoisonné un SDK officiel de Microsoft et diffusé son framework malveillant en open-source, facilitant l'émergence d'opérateurs "copieurs".

**Points clés :**
*   **Brèche GitHub :** L'utilisation de secrets volés (CVE-2026-45321) a permis de publier une version malveillante de l'extension *Nx Console* sur le Visual Studio Marketplace, entraînant l'exfiltration de 3 800 dépôts internes.
*   **SDK Microsoft Trojanisé :** Le package PyPI `durabletask` (versions 1.4.1 à 1.4.3) a été infecté, exposant les environnements cloud à un vol d'identifiants et à un *wiper* (effaceur de données) pour Linux.
*   **Vague @antv :** Une compromission massive sur npm (323 packages) a utilisé de faux badges de vérification Sigstore pour tromper les utilisateurs.
*   **Framework public :** Le code source du framework "Shai-Hulud" a été publié sur GitHub, permettant à d'autres acteurs de déployer des variantes malveillantes.

**Vulnérabilités associées :**
*   **CVE-2026-45321 :** Abus de jetons OIDC (TanStack) permettant la compromission en chaîne et la publication de logiciels malveillants via des comptes "éditeurs vérifiés".

**Recommandations de sécurité :**
*   **Réinitialisation immédiate :** Révoquer et renouveler tous les jetons CI/CD, clés API (AWS, GCP, Azure), secrets Kubernetes et mots de passe (1Password, Bitwarden) ayant transité par les environnements exposés.
*   **Audit d'intégrité :** Ne plus se fier aux badges de "éditeur vérifié" ou aux attestations UI. Verrouiller les versions exactes des dépendances et vérifier systématiquement les hashs des fichiers de verrouillage (*lockfiles*).
*   **Recherche de persistance :** Inspecter les fichiers de configuration des agents IA et des éditeurs, notamment `~/.claude/settings.json` et `.vscode/tasks.json`.
*   **Surveillance :** Analyser l'historique des sessions `kubectl exec` et AWS SSM pour détecter des mouvements latéraux après l'installation des packages compromis.

---
[Source](https://isc.sans.edu/diary/rss/33014){:target="_blank"}
