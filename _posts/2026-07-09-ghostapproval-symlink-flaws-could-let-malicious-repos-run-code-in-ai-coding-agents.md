---
title: 'GhostApproval Symlink Flaws Could Let Malicious Repos Run Code in AI Coding Agents'
date: 2026-07-09
permalink: /posts/2026/07/09/ghostapproval-symlink-flaws-could-let-malicious-repos-run-code-in-ai-coding-agents/
tags:
- veille-cyber
- hackernews
---
### GhostApproval : Vulnérabilité par liens symboliques dans les agents de codage IA

Des chercheurs de Wiz ont identifié une faille de sécurité, baptisée **GhostApproval**, affectant plusieurs assistants de codage IA (Amazon Q Developer, Claude Code, Cursor, etc.). Cette vulnérabilité permet à un dépôt de code malveillant de manipuler l'assistant pour qu'il modifie des fichiers système sensibles (comme `~/.ssh/authorized_keys` ou `~/.zshrc`) à l'insu de l'utilisateur, tout en affichant un message d'approbation trompeur indiquant un fichier inoffensif.

#### Points clés
* **Mécanisme d'attaque :** L'agent suit un lien symbolique (symlink) malicieux pointant vers un fichier système critique sans vérifier la destination réelle.
* **Faille de consentement :** Les outils présentent une boîte de dialogue de validation affichant le chemin d'accès "apparent" au lieu du chemin réel ("bypass de consentement éclairé").
* **Impact :** Exécution de code arbitraire, vol d'identifiants (clés SSH/AWS) et prise de contrôle de la machine de développement.

#### Vulnérabilités identifiées
* **CVE-2026-12958** : Amazon Q Developer (Correctif disponible).
* **CVE-2026-50549** : Cursor (Correctif disponible).
* **CVE en attente** : Google Antigravity (Correctif disponible).
* **Non corrigé à ce jour :** Augment et Windsurf.
* **Disputé :** Anthropic (Claude Code) estime que le risque relève de la responsabilité de l'utilisateur.

#### Recommandations
* **Mise à jour :** Installer immédiatement les versions corrigées des outils concernés.
* **Précautions d'usage :** Ne pas ouvrir de dépôts non approuvés avec des agents IA ; privilégier l'exécution au sein d'environnements isolés (conteneurs ou sandbox).
* **Vérification manuelle :** Après l'utilisation d'un agent dans un dépôt inconnu, inspecter les fichiers sensibles (ex: `ls -la ~/.zshrc ~/.ssh/authorized_keys`) pour détecter toute modification non autorisée.
* **Meilleures pratiques pour les développeurs :** Limiter les privilèges de lecture/écriture des agents IA et vérifier les fichiers de configuration cachés avant toute initialisation de projet.

---
[Source](https://thehackernews.com/2026/07/ghostapproval-symlink-flaws-could-let.html){:target="_blank"}
