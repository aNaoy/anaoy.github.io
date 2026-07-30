---
title: 'Microsoft Copilot for Word Can Copy Hidden Prompts Into New Documents'
date: 2026-07-30
permalink: /posts/2026/07/30/microsoft-copilot-for-word-can-copy-hidden-prompts-into-new-documents/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité d'injection de requêtes dans Microsoft Copilot pour Word

Une faille de sécurité persistante dans Microsoft 365 Copilot permet à des instructions malveillantes dissimulées dans un document Word d'être traitées par l'IA comme des commandes légitimes. Cette technique peut entraîner la manipulation de données (ex: modification de chiffres financiers) et la propagation automatique de ces instructions invisibles dans de nouveaux documents générés, créant ainsi une chaîne d'infection par propagation.

**Points clés :**
* **Mécanisme :** Le modèle confond le contenu d'un document source (utilisé comme contexte) avec les instructions utilisateur.
* **Dissimulation :** Les instructions malveillantes sont insérées dans le texte source en utilisant une mise en forme invisible (texte blanc sur fond blanc), que Copilot conserve lors de la rédaction.
* **Persistance :** Une fois qu'un document est infecté, il propage le comportement malveillant lorsqu'il est utilisé comme source pour de futures sessions Copilot.
* **État de la vulnérabilité :** Aucune CVE n'a été attribuée. Bien que Microsoft ait déployé des correctifs de filtrage, la classe de vulnérabilité reste exploitable par des variantes d'attaques.

**Vulnérabilités :**
* **Type :** Injection de requêtes indirecte (Indirect Prompt Injection / XPIA).
* **CVE :** Aucune référence CVE disponible à ce jour.

**Recommandations :**
* **Méfiance envers les sources externes :** Traiter tout document provenant de sources externes comme non fiable.
* **Audit manuel :** Vérifier systématiquement le contenu des documents joints avant de lancer une opération de génération ou d'édition via Copilot.
* **Contrôle post-génération :** Relire attentivement les fichiers produits par Copilot avant toute utilisation ou partage pour détecter d'éventuelles anomalies ou textes cachés.
* **Approche « Zero Trust » :** Garder à l'esprit que le contrôle par l'IA ne constitue pas une frontière de sécurité absolue ; les accès aux données doivent rester régis par des systèmes déterministes.

---
[Source](https://thehackernews.com/2026/07/microsoft-copilot-for-word-can-copy.html){:target="_blank"}
