---
title: 'Are Copilot prompt injection flaws vulnerabilities or AI limits?'
date: 2026-01-06
permalink: /posts/2026/01/06/are-copilot-prompt-injection-flaws-vulnerabilities-or-ai-limits/
tags:
- veille-cyber
- bleepingcomp
---
**Divergences sur le Risque de Sécurité dans Microsoft Copilot**

Une divergence d'opinions émerge quant à la qualification de certains problèmes découverts dans Microsoft Copilot comme des vulnérabilités de sécurité. Un ingénieur en cybersécurité a signalé plusieurs failles, mais Microsoft les a jugées hors de portée de ses critères de prise en charge, les considérant comme des limitations inhérentes aux systèmes d'IA plutôt que des vulnérabilités exploitables.

**Points Clés et Failles Signalées :**

*   **Injection de Prompt (Directe et Indirecte) :** Permet la divulgation du prompt système, c'est-à-dire les instructions cachées guidant le comportement de l'IA.
    *   *CVE :* Aucune CVE spécifique n'est mentionnée dans l'article.
*   **Contournement des Restrictions de Téléchargement de Fichiers :** L'encodage en base64 permet de contourner les restrictions sur les types de fichiers "risqués" qui peuvent être téléchargés. Le contenu du fichier est ensuite décodé et analysé dans la session, ignorant ainsi les contrôles de politique initiaux.
    *   *CVE :* Aucune CVE spécifique n'est mentionnée dans l'article.
*   **Exécution de Commandes dans l'Environnement Linux Isolé :** Permet l'exécution de commandes au sein de l'environnement Linux confiné de Copilot, potentiellement via une évasion de sandbox Python.
    *   *CVE :* Aucune CVE spécifique n'est mentionnée dans l'article.

**Divergence d'Interprétation :**

Certains experts considèrent ces problèmes comme des limites fondamentales des grands modèles linguistiques (LLM) qui peinent à distinguer les données des instructions. D'autres, cependant, soulignent que des assistants IA concurrents gèrent mieux ces scénarios, suggérant un manque de validation d'entrée appropriée dans Copilot. Microsoft, de son côté, applique ses critères de "bug bar", estimant que les failles rapportées ne franchissent pas de limites de sécurité claires, n'affectent pas uniquement l'environnement de l'utilisateur, ou ne fournissent que des informations de faible privilège.

**Recommandations et Perspective :**

L'article suggère que la différence de perception réside dans la définition du risque. Tandis que les chercheurs perçoivent un risque significatif, Microsoft les considère comme des comportements attendus tant qu'ils ne conduisent pas à un accès non autorisé ou à une exfiltration de données. La perspective de l'OWASP GenAI Project nuance la divulgation du prompt système, la considérant comme un risque uniquement lorsque des données sensibles sont impliquées ou lorsque le prompt sert de contrôle de sécurité. Il est reconnu que, même sans divulgation directe, les attaquants peuvent souvent déduire les restrictions du prompt par l'observation. Cette divergence dans la définition et l'évaluation du risque est susceptible de persister avec l'adoption croissante de ces outils.

---
[Source](https://www.bleepingcomputer.com/news/security/are-copilot-prompt-injection-flaws-vulnerabilities-or-ai-limits/){:target="_blank"}
