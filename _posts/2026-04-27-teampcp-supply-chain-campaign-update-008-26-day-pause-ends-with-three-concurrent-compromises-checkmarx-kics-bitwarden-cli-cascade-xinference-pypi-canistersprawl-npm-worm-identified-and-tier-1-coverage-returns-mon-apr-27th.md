---
title: 'TeamPCP Supply Chain Campaign: Update 008 - 26-Day Pause Ends with Three Concurrent Compromises (Checkmarx KICS, Bitwarden CLI Cascade, xinference PyPI), CanisterSprawl npm Worm Identified, and Tier 1 Coverage Returns, (Mon, Apr 27th)'
date: 2026-04-27
permalink: /posts/2026/04/27/teampcp-supply-chain-campaign-update-008-26-day-pause-ends-with-three-concurrent-compromises-checkmarx-kics-bitwarden-cli-cascade-xinference-pypi-canistersprawl-npm-worm-identified-and-tier-1-coverage-returns-mon-apr-27th/
tags:
- veille-cyber
- sans-isc
---
### Résurgence des attaques de la chaîne d’approvisionnement par TeamPCP

Après une pause de 26 jours, le groupe cybercriminel TeamPCP (UNC6780) a repris ses activités offensives avec trois compromissions simultanées sur les écosystèmes npm, PyPI et Docker Hub entre le 21 et le 22 avril 2026. Cette phase marque un retour à des opérations d'intrusion active visant à dérober des identifiants au sein des pipelines CI/CD.

**Points clés :**
*   **Propagation en cascade :** La compromission de l'image Docker `checkmarx/kics` a entraîné l'infection automatique de `@bitwarden/cli` (version 2026.4.0) via les outils d'automatisation (Dependabot), illustrant le risque majeur des dépendances automatisées.
*   **Vers de chaîne d’approvisionnement :** Identification de *CanisterSprawl*, un ver npm auto-propageant capable de voler des identifiants et de basculer de npm vers PyPI si des jetons de publication sont détectés.
*   **Stratégie ambiguë :** Le groupe revendique certaines attaques (Checkmarx) tout en en niant d'autres (xinference), malgré des signatures techniques quasi identiques, suggérant une stratégie de "fausse bannière" ou une priorisation basée sur le prestige des cibles.

**Vulnérabilités et vecteurs d'attaque :**
*   **CanisterSprawl :** Utilisation de scripts `postinstall` malveillants pour l'exécution automatique.
*   **Checkmarx KICS :** Détournement des comptes de publication officiels sur Docker Hub ; injection de charges utiles dans les extensions VS Code/Open VSX via des commits GitHub.
*   **Bitwarden CLI :** Infection via l'automatisation de build (Dependabot).
*   **CVE-2026-33634 :** Mentionnée comme point de référence pour les délais de remédiation CISA (non spécifique à cet incident mais critique pour le contexte).

**Recommandations :**
*   **Sécurisation CI/CD :** Auditer les configurations des outils d'automatisation des dépendances (ex: Dependabot) pour éviter l'import automatique d'images ou de paquets non vérifiés.
*   **Vérification d'intégrité :** Appliquer systématiquement une vérification d'intégrité (signature numérique) pour toutes les images conteneurs et extensions VS Code avant exécution.
*   **Surveillance des jetons :** Révoquer et renouveler les jetons d'API (GitHub, npm, Cloud, SSH) pour toute organisation ayant utilisé les versions compromises de KICS ou Bitwarden CLI durant la fenêtre du 22 avril 2026.
*   **Veille proactive :** Surveiller les comportements réseau suspects émanant des environnements de build vers des infrastructures C2 non identifiées (ex: protocoles basés sur ICP - *Internet Computer Protocol*).

---
[Source](https://isc.sans.edu/diary/rss/32926){:target="_blank"}
