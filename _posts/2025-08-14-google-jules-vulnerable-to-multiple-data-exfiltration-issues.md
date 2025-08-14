---
title: 'Google Jules: Vulnerable to Multiple Data Exfiltration Issues'
date: 2025-08-14
permalink: /posts/2025/08/14/google-jules-vulnerable-to-multiple-data-exfiltration-issues/
tags:
- veille-cyber
- zerodaysfans
---
### Fuites d'informations dans l'agent de codage Google Jules

L'agent de codage asynchrone Google Jules présente plusieurs vulnérabilités permettant l'exfiltration de données sensibles via des attaques par injection de prompt. Ces failles permettent à des acteurs malveillants d'extraire des informations de Jules et de les envoyer à des serveurs externes.

**Points Clés :**

*   Google Jules semble utiliser plusieurs agents, un agent principal proposant un plan et des agents "workers" exécutant des sous-tâches avec différents outils.
*   Les vulnérabilités découvertes permettent de contourner le mécanisme d'approbation humaine avant l'exécution des tâches.
*   Ces failles ont été communiquées à Google en mai 2025.

**Vecteurs d'Exfiltration :**

1.  **Rendu d'image via la syntaxe Markdown :** Jules peut être incité à charger une page web spécifique qui contient des instructions malveillantes. Il peut ensuite utiliser ces instructions pour envoyer des données d'une conversation précédente à une URL tierce en guise de chargement d'image.
2.  **Utilisation de l'outil `view_text_website` :** Cet outil, destiné à lire le contenu des sites web, peut être détourné pour envoyer des données vers une URL contrôlée par l'attaquant. Il est possible de lire des fichiers présents sur la machine Jules et d'exfiltrer leur contenu.

Ces deux vecteurs peuvent être déclenchés sans nécessiter l'intervention d'un agent "worker" ou l'approbation du plan par l'utilisateur, ce qui rend l'attaque potentiellement plus rapide et plus difficile à détecter.

**Recommandations et Mitigations :**

*   **Pour le rendu d'image :** Implémenter une politique de sécurité de contenu (CSP) pour restreindre le chargement de ressources à des emplacements de confiance, ou envisager de ne pas rendre d'images du tout.
*   **Pour l'outil `view_text_website` :**
    *   Mettre en place une liste blanche configurable de domaines autorisés (similaire à ChatGPT Codex).
    *   Demander une approbation humaine avant chaque appel à cet outil.
    *   Afficher clairement dans le plan proposé toutes les communications externes et ne pas se connecter à des domaines non explicitement listés dans le plan.
*   **Pour les utilisateurs :** Faire preuve de prudence en fournissant des informations sensibles aux agents de codage asynchrones et examiner attentivement les plans proposés par Jules pour détecter toute tentative de communication externe suspecte.

---
[Source](https://embracethered.com/blog/posts/2025/google-jules-vulnerable-to-data-exfiltration-issues/){:target="_blank"}
