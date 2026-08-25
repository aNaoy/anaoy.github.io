---
title: 'Marimo Notebook Flaw Could Run MCP Commands Before Cells Execute in Edit Mode'
date: 2026-08-25
permalink: /posts/2026/08/25/marimo-notebook-flaw-could-run-mcp-commands-before-cells-execute-in-edit-mode/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique d'injection de code dans Marimo Notebook

Une faille de sécurité majeure dans Marimo Notebook permet à un attaquant d'exécuter des commandes arbitraires sur le système local dès l'ouverture d'un notebook piégé en mode édition, avant même l'exécution des cellules.

**Points clés :**
*   **Vecteur d'attaque :** La vulnérabilité exploite la manière dont Marimo traite les configurations fournies dans les métadonnées du notebook (notamment via le protocole MCP).
*   **Impact :** Un attaquant peut forcer l'exécution de commandes sous forme de sous-processus local sans authentification préalable, nécessitant uniquement une interaction utilisateur (ouvrir le notebook).
*   **Contexte :** Cette correction s'inscrit dans un effort plus large de sécurisation des métadonnées PEP 723 pour empêcher l'injection de configurations malveillantes.

**Vulnérabilités identifiées :**
*   **CVE-2026-75149 :** Faille d'injection de code (Score CVSS v4 : 8.7 / v3.1 : 8.8). Affecte les versions antérieures à 0.23.15.
*   **CVE-2026-67618 :** Faille distincte permettant l'exfiltration de clés API via des points de terminaison IA malveillants, également corrigée dans la version 0.23.15.

**Recommandations :**
*   **Mise à jour immédiate :** Les utilisateurs doivent mettre à jour Marimo vers la version **0.23.15 ou ultérieure** (la version actuelle recommandée étant la 0.24.0).
*   **Précautions :** Éviter d'ouvrir des notebooks provenant de sources non fiables. La mise à jour applique une liste blanche stricte sur les configurations de métadonnées, supprimant les sections sensibles (ai, mcp, secrets, etc.) potentiellement manipulées par des attaquants.

---
[Source](https://thehackernews.com/2026/08/marimo-notebook-flaw-could-run-mcp.html){:target="_blank"}
