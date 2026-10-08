---
title: 'Tensorlake npm Package Compromised to Deliver Shai-Hulud Credential-Stealing Worm'
date: 2026-10-08
permalink: /posts/2026/10/08/tensorlake-npm-package-compromised-to-deliver-shai-hulud-credential-stealing-worm/
tags:
- veille-cyber
- hackernews
---
### Compromission de la supply chain : Le ver "Shai-Hulud" cible le package npm Tensorlake

Le package npm `tensorlake` (version 0.5.144) a été compromis dans le cadre d'une attaque de type *ChainDrop / Shai-Hulud*. Cette version malveillante intègre un ver informatique capable d'exfiltrer des données sensibles, d'établir une persistance sur les systèmes infectés et d'exécuter du code à distance.

**Points clés :**
*   **Mécanisme d'infection :** L'attaque utilise un *preinstall hook* pour lancer un chargeur obfusqué (basé sur le runtime Bun), qui déploie ensuite le ver principal.
*   **Capacités de propagation :** Le ver énumère les identités de publication npm de la victime, génère des preuves de provenance (Sigstore) et republie automatiquement des versions compromises.
*   **Persistance avancée :** Le logiciel malveillant modifie des fichiers de configuration (`.claude/settings.json`, `.vscode/tasks.json`) pour se réexécuter lors de l'utilisation d'outils comme Claude Code ou VS Code.
*   **Technique du "Jeton Otage" :** Un script PowerShell surveille la validité des jetons GitHub volés. Si la victime révoque son jeton, le script déclenche une routine destructive.

**Données visées :**
Le malware exfiltre une large gamme de secrets : tokens npm et GitHub, clés AWS, identifiants Kubernetes, clés SSH, fichiers `.env`, portefeuilles de cryptomonnaies, et données de configuration pour divers agents IA (Claude, Cursor, Kiro, etc.).

**Vulnérabilités :**
Aucune CVE spécifique n'est associée, car il s'agit d'une attaque directe sur la chaîne d'approvisionnement logicielle via la compromission du dépôt source du mainteneur.

**Recommandations :**
*   **Suppression immédiate :** Désinstaller la version 0.5.144 du package `tensorlake` si elle a été installée.
*   **Rotation des secrets :** Considérer tous les identifiants présents sur les machines ayant utilisé cette version comme compromis. Il est impératif de révoquer et de renouveler tous les jetons, clés API, clés SSH et mots de passe stockés sur ces environnements.
*   **Audit de sécurité :** Vérifier les dépôts GitHub et les workflows CI/CD pour détecter toute activité suspecte ou création de nouveaux flux de travail non autorisés.

---
[Source](https://thehackernews.com/2026/10/tensorlake-npm-package-compromised-to.html){:target="_blank"}
