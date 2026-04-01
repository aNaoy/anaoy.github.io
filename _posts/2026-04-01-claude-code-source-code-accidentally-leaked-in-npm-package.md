---
title: 'Claude Code source code accidentally leaked in NPM package'
date: 2026-04-01
permalink: /posts/2026/04/01/claude-code-source-code-accidentally-leaked-in-npm-package/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite accidentelle du code source de Claude Code sur NPM

Anthropic a involontairement rendu public le code source propriétaire de son outil "Claude Code" via une mise à jour sur le registre NPM. Cet incident est dû à une erreur humaine lors du processus de conditionnement du paquet (version 2.1.88).

**Points clés :**
* **Nature de la fuite :** L'inclusion d'un fichier `cli.js.map` (source map) contenant l'intégralité du code source original (environ 1 900 fichiers et 500 000 lignes de code).
* **Impact :** Aucune donnée client ou identifiant sensible n'a été compromis. Anthropic a confirmé qu'il s'agissait d'une erreur technique et non d'une intrusion.
* **Conséquences :** Le code s'est largement diffusé sur GitHub, poussant Anthropic à émettre des notifications de retrait DMCA. Des fonctionnalités internes inédites, telles que les modes « Proactive » et « Dream », ont été révélées par l'analyse du code.
* **Problème annexe :** Anthropic enquête simultanément sur un bug entraînant une consommation anormalement rapide des limites d'utilisation de Claude Code, provoquant des interruptions de service pour les utilisateurs.

**Vulnérabilités :**
* Aucune CVE n'est associée, car il s'agit d'une erreur de configuration de packaging (fuite de fichiers de débogage contenant des sources intégrées).

**Recommandations pour les développeurs et entreprises :**
* **Sécurisation des processus de build :** S'assurer que les fichiers de "source map" générés lors de la compilation ne contiennent pas le champ `sourcesContent`, ou supprimer systématiquement ces fichiers avant toute publication sur des registres publics.
* **Audit des paquets :** Mettre en place des contrôles automatisés pour vérifier le contenu des archives (paquets NPM, Docker images, etc.) avant leur déploiement afin de détecter l'inclusion accidentelle de fichiers sensibles ou de débogage.
* **Réponse aux incidents :** En cas de fuite de propriété intellectuelle, agir rapidement via des demandes de retrait (DMCA) pour limiter la prolifération du code sur les plateformes tierces.

---
[Source](https://www.bleepingcomputer.com/news/artificial-intelligence/claude-code-source-code-accidentally-leaked-in-npm-package/){:target="_blank"}
