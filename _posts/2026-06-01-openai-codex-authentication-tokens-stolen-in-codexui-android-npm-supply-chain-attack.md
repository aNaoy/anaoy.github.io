---
title: 'OpenAI Codex Authentication Tokens Stolen in codexui-android npm Supply Chain Attack'
date: 2026-06-01
permalink: /posts/2026/06/01/openai-codex-authentication-tokens-stolen-in-codexui-android-npm-supply-chain-attack/
tags:
- veille-cyber
- hackernews
---
### Vol de jetons d'authentification OpenAI Codex via la supply chain

Une campagne malveillante cible les développeurs utilisant OpenAI Codex via le package npm `codexui-android` et plusieurs applications Android associées. Le code malveillant, intégré dans des versions légitimes, exfiltre silencieusement les jetons d'authentification des utilisateurs vers un serveur distant contrôlé par l'attaquant.

**Points clés :**
* **Vecteur d'attaque :** Le package npm `codexui-android` (plus de 29 000 téléchargements) et des applications Android comme "OpenClaw Codex Claude AI Agent" et "Codex".
* **Méthode :** Utilisation d'un environnement sandbox (PRoot) dans les applications mobiles pour exécuter le package npm malveillant, qui accède au fichier local `~/.codex/auth.json` contenant les jetons d'accès.
* **Impact :** Vol des `access_token`, `refresh_token` et `id_token`. Le jeton de rafraîchissement (refresh_token) n'expirant pas, l'attaquant bénéficie d'un accès persistant et illimité au compte OpenAI de la victime.
* **Masquage :** Les données sont exfiltrées vers un domaine (`sentry.anyclaw[.]store`) se faisant passer pour la plateforme Sentry.

**Vulnérabilités :**
* Stockage des jetons d'authentification en clair dans un fichier local (`~/.codex/auth.json`), facilitant leur exfiltration par tout processus malveillant ayant accès au système de fichiers.
* Absence de pinning de version dans le package npm, permettant l'exécution automatique de versions compromises.

**Recommandations :**
* **Révoquer immédiatement** les clés API et régénérer les jetons d'authentification associés à OpenAI Codex si vous avez utilisé les outils suspects.
* **Sécuriser les secrets :** Ne jamais stocker de jetons d'authentification en clair sur le disque. Utiliser des gestionnaires de secrets ou des outils de stockage sécurisés fournis par le système d'exploitation.
* **Audit des dépendances :** Vérifier les packages npm installés et surveiller les comportements réseau inhabituels émanant des outils de développement.
* **Vigilance mobile :** Se méfier des applications tierces prétendant offrir des interfaces pour des services IA, surtout si elles demandent des accès étendus ou intègrent des environnements d'exécution complexes (Node.js/PRoot).

---
[Source](https://thehackernews.com/2026/06/openai-codex-authentication-tokens.html){:target="_blank"}
