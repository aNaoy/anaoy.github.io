---
title: 'Git Patches Flaw That Lets Malicious Repositories Execute Code During Recursive Clones'
date: 2026-11-11
permalink: /posts/2026/11/11/git-patches-flaw-that-lets-malicious-repositories-execute-code-during-recursive-clones/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans Git : Exécution de code et corruption mémoire

Une série de failles de sécurité majeures a été corrigée dans Git, incluant un vecteur d'exécution de code à distance lors de clones récursifs.

**Points clés :**
*   **Risque principal :** Un attaquant peut manipuler des chemins de fichiers extrêmement longs pour outrepasser les contrôles de sécurité et remplacer le fichier `.git` d'un sous-module par un lien symbolique pointant vers des scripts malveillants.
*   **Surface d'attaque :** Les opérations de clonage récursif de dépôts non approuvés constituent le vecteur d'infection principal.
*   **Correctifs :** La mise à jour vers la version 2.56.1 (ou versions corrigées correspondantes pour les séries 2.50 à 2.55) est impérative.

**Vulnérabilités identifiées :**
*   **CVE-2026-111760 :** Troncature d'entier permettant l'écrasement de fichiers via un chemin de dépôt malicieux (exécution de code).
*   **CVE-2026-113408 :** Traversée de répertoire lors du clonage de dépôts vides via le protocole v2.
*   **CVE-2026-114467 :** Corruption de la mémoire pile lors de la fusion de tags contenant plusieurs signatures GPG (déni de service).
*   **CVE-2026-114469 :** Dépassement de capacité lors du traitement de patchs binaires (lecture hors limites).
*   **CVE-2026-105437 :** Corruption du tas lors de fusions complexes avec des attributs `conflict-marker-size` malveillants.
*   **CVE-2026-114466 :** Exploitation de fonctionnalités `fast-import` pour la lecture ou l'écriture arbitraire de fichiers.

**Recommandations :**
*   **Mise à jour immédiate :** Installez la version 2.56.1 ou supérieure. Si vous utilisez des outils intégrés (GitHub Desktop, Copilot), mettez-les également à jour dès que les correctifs sont disponibles.
*   **Gestion des serveurs :** Les administrateurs d'instances GitHub Enterprise doivent appliquer les versions corrigées (ex: 3.22.4).
*   **Mesures conservatoires :** En attendant la mise à jour, ne clonez, ne fusionnez et n'utilisez que des dépôts ou patchs provenant de sources strictement fiables.
*   **Atténuation temporaire (pour CVE-2026-105437) :** Forcez `conflict-marker-size=7` dans les fichiers `info/attributes` sur les serveurs hébergeant du code.

---
[Source](https://thehackernews.com/2026/11/git-patches-flaw-that-lets-malicious.html){:target="_blank"}
