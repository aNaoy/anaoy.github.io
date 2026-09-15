---
title: 'Homebrew 7.0.0 gets built-in GUI, better security controls'
date: 2026-09-15
permalink: /posts/2026/09/15/homebrew-700-gets-built-in-gui-better-security-controls/
tags:
- veille-cyber
- bleepingcomp
---
### Homebrew 7.0.0 : Renforcement de la sécurité et nouvelle interface

La version 7.0.0 du gestionnaire de paquets Homebrew introduit des fonctionnalités de sécurité majeures et une interface graphique native, BrewUI, facilitant la gestion des dépendances sur macOS. Cette mise à jour répond aux menaces croissantes, telles que les malwares de type "info-stealer" ciblant régulièrement l'outil.

**Points clés :**
*   **Scanner de vulnérabilités intégré :** Introduction de la commande `brew vulns` permettant d'analyser les paquets installés ou déclarés dans un `Brewfile`.
*   **Base de données d'avis dédiée :** Publication d'avis au format OSV (Open Source Vulnerability) spécifiques à Homebrew, incluant les correctifs rétroportés (backported) qui ne modifient pas la version amont du logiciel.
*   **Intégration OSV.dev :** Le scanner interroge automatiquement la base OSV.dev pour vérifier les correspondances de vulnérabilités et croiser les données avec les correctifs déjà appliqués par Homebrew.
*   **Sandboxing amélioré :** Restriction par défaut de l'accès aux répertoires personnels des utilisateurs et séparation accrue entre le téléchargement des dépendances et l'installation hors ligne.
*   **Interface BrewUI :** Nouvel outil graphique pour macOS 26+ permettant une gestion visuelle des paquets et de leurs dépendances.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, car cette mise à jour se concentre sur l'outillage de détection générique pour prévenir l'exploitation de failles connues dans les paquets tiers.

**Recommandations :**
*   **Mise à jour :** Passer immédiatement à Homebrew 7.0.0 pour bénéficier des correctifs de sécurité et du nouveau mécanisme de sandboxing.
*   **Audit proactif :** Utiliser régulièrement la commande `brew vulns` pour identifier les composants obsolètes ou vulnérables au sein de l'environnement de développement.
*   **Veille :** Intégrer la base d'avis OSV de Homebrew dans les flux de surveillance des vulnérabilités pour automatiser la détection des failles sur les paquets gérés.

---
[Source](https://www.bleepingcomputer.com/news/security/homebrew-700-gets-built-in-gui-better-security-controls/){:target="_blank"}
