---
title: 'Power Grid Model Security Audit'
date: 2026-10-13
permalink: /posts/2026/10/13/power-grid-model-security-audit/
tags:
- veille-cyber
- zerodaysfans
---
### Audit de sécurité de Power Grid Model (PGM)

L'audit de la bibliothèque open-source **Power Grid Model** (développée par LF Energy), mené par Shielder sous l'égide de l'OSTIF, a révélé des vulnérabilités critiques liées au traitement des données d'entrée, à la manipulation de fichiers de configuration et à la gestion de la mémoire dans son cœur C++.

#### Vulnérabilités identifiées

*   **CVE-2026-84457 (Sévérité : Élevée) :** Exécution arbitraire de méthodes via les fichiers de mapping YAML. Le convertisseur permettait de référencer des fonctions Python arbitraires sans contrôle, facilitant l'exécution de code à distance (RCE).
*   **CVE-2026-76912 (Sévérité : Moyenne) :** Déni de service (DoS) par imbrication JSON illimitée. L'absence de limite de profondeur dans le parsing JSON permettait de saturer la mémoire et de provoquer l'arrêt du processus.
*   **CVE-2026-76911 (Sévérité : Faible) :** Accès mémoire hors limites (Out-Of-Bounds) lors du calcul de scénarios. Une validation insuffisante de l'indexation des buffers (`indptr`) permettait des accès mémoire invalides, entraînant un risque de DoS.

#### Points clés de l'analyse
*   **Surface d'attaque :** Les vecteurs principaux sont les pipelines de désérialisation (JSON/msgpack) et les convertisseurs de fichiers (YAML).
*   **Langage :** Le cœur en C++ est sensible aux problèmes de sécurité mémoire, bien que le wrapper Python intègre des validations robustes limitant l'exploitabilité directe.
*   **Supply Chain :** Les workflows GitHub utilisés pour les déploiements présentaient des risques, notamment l'absence de hachage lors du téléchargement des dépendances de build.

#### Recommandations
*   **Correctifs immédiats :** Mettre à jour `power-grid-model-io` (v2.0.0+) et `power-grid-model` (v1.13.115+) pour bénéficier des correctifs de sécurité.
*   **Gestion des dépendances :** Verrouiller les dépendances de build via des hash SHA-256 dans les fichiers de configuration (ex: `pyproject.toml`) pour éviter les attaques sur la chaîne d'approvisionnement.
*   **Sécurisation du code :** 
    *   Remplacer les assertions C++ (`narrow_cast`) par des exceptions vérifiées pour éviter qu'elles ne soient ignorées en mode production.
    *   Activer l'outil **UBSan** (UndefinedBehaviorSanitizer) dans les pipelines de tests pour détecter les comportements indéfinis.
*   **Transparence :** Générer et publier une nomenclature logicielle (SBOM) au format CycloneDX ou SPDX à chaque release.
*   **Précautions d'usage :** Considérer les fichiers de mapping YAML comme du code exécutable et ne jamais charger de configurations provenant de sources non fiables.

---
[Source](https://www.shielder.com/blog/2026/10/power-grid-model-security-audit/){:target="_blank"}
