---
title: 'Compromised Nx Console 18.95.0 Targeted VS Code Developers with Credential Stealer'
date: 2026-05-19
permalink: /posts/2026/05/19/compromised-nx-console-18950-targeted-vs-code-developers-with-credential-stealer/
tags:
- veille-cyber
- hackernews
---
### Compromission de l'extension Nx Console : une menace pour la chaîne d'approvisionnement

La version 18.95.0 de l'extension **Nx Console** pour VS Code a été compromise, exposant plus de 2,2 millions d'installations à une attaque par chaîne d'approvisionnement. L'incident a été causé par le piratage du compte GitHub d'un développeur de l'extension, permettant aux attaquants d'injecter un code malveillant via un commit non signé.

**Points clés :**
*   **Mode opératoire :** L'extension exécute silencieusement un payload obfuscé dès l'ouverture d'un espace de travail.
*   **Capacités du malware :** Vol d'identifiants (GitHub, AWS, npm, 1Password, Claude Code), installation d'une porte dérobée Python sur macOS, et utilisation de Sigstore pour générer des preuves de provenance falsifiées.
*   **Risque accru :** En signant les paquets malveillants, les attaquants peuvent faire apparaître des logiciels corrompus comme étant légitimes et vérifiés.
*   **Contexte :** Cette attaque s'inscrit dans une vague massive de malwares sur npm visant le vol de données et le contrôle à distance.

**Vulnérabilités :**
Aucune CVE spécifique n'est associée, l'attaque reposant sur l'injection de code via des identifiants de développeur compromis et une mauvaise gestion des commits dans le dépôt officiel.

**Recommandations :**
*   **Mise à jour immédiate :** Passer à la version 18.100.0 ou ultérieure de Nx Console.
*   **Nettoyage système :** Supprimer les fichiers suspects (`~/.local/share/kitty/cat.py`, `~/Library/LaunchAgents/com.user.kitty-monitor.plist`, etc.) et tuer les processus associés (notamment `cat.py`).
*   **Rotation des secrets :** Réinitialiser impérativement tous les jetons, clés SSH, secrets AWS/npm et identifiants stockés sur les machines ayant utilisé la version 18.95.0.

---
[Source](https://thehackernews.com/2026/05/compromised-nx-console-18950-targeted.html){:target="_blank"}
