---
title: 'DirectX, OpenFOAM, Libbiosig vulnerabilities'
date: 2026-03-12
permalink: /posts/2026/03/12/directx-openfoam-libbiosig-vulnerabilities/
tags:
- veille-cyber
- zerodaysfans
---
### Vulnérabilités critiques : DirectX, OpenFOAM et Libbiosig

L'équipe de recherche de Cisco Talos a identifié plusieurs failles de sécurité majeures dans des logiciels largement utilisés, allant de l'élévation de privilèges à l'exécution de code arbitraire.

**Points clés :**
*   **Microsoft DirectX :** Une faille locale d'élévation de privilèges affectant le processus d'installation du runtime DirectX.
*   **OpenFOAM :** Une vulnérabilité critique permettant l'exécution de code arbitraire via la manipulation de fichiers de simulation.
*   **Libbiosig :** Plusieurs failles (fuite d'informations et exécution de code) exploitables via des fichiers de données biomédicales malveillants.

**Vulnérabilités identifiées :**

| Logiciel | Type de vulnérabilité | Référence CVE |
| :--- | :--- | :--- |
| **Microsoft DirectX** | Élévation de privilèges (LPE) | CVE-2025-68623 |
| **OpenFOAM** | Exécution de code arbitraire | CVE-2025-61982 |
| **Libbiosig** | Lecture hors limites (fuite d'info) | CVE-2025-64736 |
| **Libbiosig** | Débordement de tampon (heap) | CVE-2026-22891 |
| **Libbiosig** | Débordement de tampon (heap) | CVE-2026-20777 |

**Recommandations :**
*   **Mises à jour :** Appliquer immédiatement les correctifs fournis par les éditeurs pour OpenFOAM et Libbiosig.
*   **Surveillance :** Pour Microsoft DirectX, bien que la vulnérabilité ne soit pas encore corrigée, il est conseillé de surveiller les installations de composants legacy.
*   **Détection :** Utiliser les jeux de règles Snort disponibles sur *Snort.org* pour identifier les tentatives d'exploitation de ces vulnérabilités sur le réseau.
*   **Vigilance :** Ne pas ouvrir de fichiers de simulation (OpenFOAM) ou de données biomédicales (.abf, .clp, .wft) provenant de sources non fiables.

---
[Source](https://blog.talosintelligence.com/directx-openfoam-libbiosig-vulnerabilities/){:target="_blank"}
