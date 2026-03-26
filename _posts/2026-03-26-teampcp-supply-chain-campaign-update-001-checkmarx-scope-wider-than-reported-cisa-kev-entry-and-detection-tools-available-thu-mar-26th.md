---
title: 'TeamPCP Supply Chain Campaign: Update 001 - Checkmarx Scope Wider Than Reported, CISA KEV Entry, and Detection Tools Available, (Thu, Mar 26th)'
date: 2026-03-26
permalink: /posts/2026/03/26/teampcp-supply-chain-campaign-update-001-checkmarx-scope-wider-than-reported-cisa-kev-entry-and-detection-tools-available-thu-mar-26th/
tags:
- veille-cyber
- sans-isc
---
### Analyse de la campagne de supply chain TeamPCP : Extension des compromissions et outils de détection

La campagne « TeamPCP » continue de cibler systématiquement les outils de sécurité, avec de nouvelles révélations sur l'ampleur des compromissions et l'ajout de vulnérabilités critiques au catalogue CISA KEV.

**Points clés :**
*   **Checkmarx `ast-github-action` :** Contrairement aux rapports initiaux, les 91 versions (tags) de l'outil ont été compromises. Chaque version a été individuellement corrompue pour dérober des identifiants.
*   **LiteLLM :** Bien que la quarantaine sur PyPI soit levée, l'éditeur a gelé toute nouvelle version. La version v1.82.6.rc.2 est la dernière considérée comme sûre.
*   **Stratégie de l'attaquant :** TeamPCP cible délibérément les outils de sécurité (Trivy, KICS, Checkmarx) pour maximiser l'impact sur les chaînes d'approvisionnement logicielles.

**Vulnérabilités et menaces :**
*   **CVE-2026-33634 (CVSS 9.4) :** Ajoutée au catalogue KEV de la CISA. Activement exploitée, elle nécessite une remédiation urgente.
*   **Compromission d'identifiants :** Toute utilisation des outils infectés (Checkmarx `ast-github-action` entre le 23 mars, 12:58 et 19:16 UTC, ou LiteLLM versions 1.82.7/1.82.8) doit être traitée comme une fuite de secrets.

**Recommandations :**
1.  **Audit CI/CD :** Rechercher toute exécution de `checkmarx/ast-github-action` durant la fenêtre de compromission du 23 mars. Révoquer et renouveler immédiatement tous les secrets accessibles par ces workflows.
2.  **Mise à jour des outils :**
    *   **Trivy :** Utiliser la version ≥ v0.69.2 (binaire) ou v0.35.0 (action).
    *   **Checkmarx :** Migrer vers la version v2.3.33.
3.  **Détection :** Utiliser les outils communautaires disponibles pour scanner les environnements :
    *   [jthack/litellm-vuln-detector](https://github.com/jthack/litellm-vuln-detector) pour détecter les backdoors et les pods malveillants.
    *   Scripts de détection des indicateurs TeamPCP.
4.  **Gestion des secrets :** Considérer comme compromis tout identifiant ou jeton ayant transité par les systèmes où les versions infectées de LiteLLM ont été installées.

---
[Source](https://isc.sans.edu/diary/rss/32834){:target="_blank"}
