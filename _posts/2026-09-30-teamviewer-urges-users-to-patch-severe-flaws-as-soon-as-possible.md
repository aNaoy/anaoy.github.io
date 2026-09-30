---
title: 'TeamViewer urges users to patch severe flaws “as soon as possible”'
date: 2026-09-30
permalink: /posts/2026/09/30/teamviewer-urges-users-to-patch-severe-flaws-as-soon-as-possible/
tags:
- veille-cyber
- bleepingcomp
---
### Alerte de sécurité critique sur TeamViewer

TeamViewer a publié un correctif d'urgence pour corriger cinq vulnérabilités critiques affectant ses solutions logicielles (Full Client et Host) sur Windows, Linux et macOS. Bien qu'aucune exploitation active ne soit actuellement recensée, la criticité des failles impose une mise à jour immédiate.

**Points clés**
*   Les vulnérabilités permettent une exécution de code à distance (RCE) ou une élévation de privilèges.
*   Les failles concernent les versions précédentes à la version 15.82.
*   Aucune preuve d'exploitation sauvage ou de code d'exploitation public n'a été détectée à ce jour.

**Vulnérabilités identifiées**
*   **CVE-2026-92370 :** Contournement du contrôle d'accès permettant une exécution de code à distance (faille la plus critique).
*   **CVE-2026-19743 :** Traversée de répertoire (path traversal).
*   **CVE-2026-92368 :** Dépassement de tampon basé sur le tas (heap-based buffer overflow).
*   **CVE-2026-92369 :** Condition de concurrence (TOCTOU).
*   **CVE-2026-92371 :** Validation de chemin incorrecte.

**Recommandations**
*   Mettre à jour vers la version **15.82** (incluant les versions de maintenance et les versions héritées supportées) dans les plus brefs délais.
*   Appliquer les mises à jour sur l'ensemble des clients et hôtes déployés au sein du parc informatique.

---
[Source](https://www.bleepingcomputer.com/news/security/teamviewer-urges-users-to-patch-severe-flaws-as-soon-as-possible/){:target="_blank"}
