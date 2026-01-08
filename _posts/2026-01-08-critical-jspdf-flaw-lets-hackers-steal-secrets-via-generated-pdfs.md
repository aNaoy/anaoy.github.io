---
title: 'Critical jsPDF flaw lets hackers steal secrets via generated PDFs'
date: 2026-01-08
permalink: /posts/2026/01/08/critical-jspdf-flaw-lets-hackers-steal-secrets-via-generated-pdfs/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite de données critique dans jsPDF

Une vulnérabilité majeure dans la bibliothèque JavaScript jsPDF permet aux attaquants de voler des informations sensibles du système de fichiers local. Cette faille, identifiée sous le nom de **CVE-2025-68428**, est une inclusion de fichier local et un parcours de répertoire qui affecte les versions antérieures à 4.0. La bibliothèque, utilisée par plus de 3,5 millions de projets hebdomadaires, peut incorporer le contenu de fichiers locaux dans les documents PDF générés si un chemin non nettoyé est fourni à la fonction `loadFile`. D'autres fonctions telles que `addImage`, `html`, et `addFont` sont également touchées car elles peuvent appeler `loadFile`.

**Points clés :**

*   **Vulnérabilité :** Inclusion de fichier local et parcours de répertoire.
*   **Impact :** Vol potentiel de données sensibles du système de fichiers local.
*   **Bibliothèque affectée :** jsPDF (versions avant 4.0).
*   **Environnement concerné :** Uniquement les versions Node.js de la bibliothèque (`dist/jspdf.node.js` et `dist/jspdf.node.min.js`).
*   **Gravité :** 9.2 sur 10.

**Vulnérabilités :**

*   **CVE-2025-68428**

**Recommandations :**

*   **Mettre à jour jsPDF :** Passer à la version 4.0.0 ou une version ultérieure (notamment les versions 22.13.0, 23.5.0, ou 24.0.0 et suivantes sont recommandées car le mode de permission de Node.js, utilisé dans la correction, est encore expérimental dans Node 20).
*   **Pour les anciennes versions de Node.js :** Nettoyer systématiquement les chemins de fichiers fournis par les utilisateurs avant de les passer à jsPDF.
*   **Configuration des permissions :** Si l'option `--permission` est utilisée, être conscient qu'elle affecte l'ensemble du processus Node.js. Éviter de configurer des permissions de système de fichiers trop larges avec `--allow-fs-read`, car cela pourrait annuler la correction.

Le risque d'exploitation est considéré comme faible à inexistant si les chemins de fichiers sont codés en dur, proviennent d'une source de confiance, ou si des listes blanches strictes sont utilisées. Cependant, compte tenu de sa large diffusion, cette vulnérabilité est une cible potentielle pour des attaques actives.

---
[Source](https://www.bleepingcomputer.com/news/security/critical-jspdf-flaw-lets-hackers-steal-secrets-via-generated-pdfs/){:target="_blank"}
