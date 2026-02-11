---
title: 'Scary Agent Skills: Hidden Unicode Instructions in Skills ...And How To Catch Them'
date: 2026-02-11
permalink: /posts/2026/02/11/scary-agent-skills-hidden-unicode-instructions-in-skills-and-how-to-catch-them/
tags:
- veille-cyber
- zerodaysfans
---
### Risques cachés dans les "Skills" pour agents IA

Les "Skills", des extensions ajoutant des fonctionnalités aux agents IA via des fichiers Markdown, représentent une surface d'attaque préoccupante. Bien qu'ils simplifient l'intégration de nouvelles capacités, ils ouvrent la porte à des vulnérabilités de type injection de prompt et d'attaques de la chaîne d'approvisionnement.

#### Points Clés

*   **Injection de prompt cachée :** Des instructions malveillantes peuvent être dissimulées dans les métadonnées des Skills (nom, description) ou via des caractères Unicode invisibles interprétés par certains modèles d'IA comme des commandes.
*   **Chaos écosystémique :** L'écosystème des Skills est fragmenté entre différents fournisseurs (OpenAI, Gemini, Claude), chacun ayant ses propres emplacements et priorités pour le stockage des Skills, rendant la gestion complexe.
*   **Modification d'environnement :** Les agents IA capables de créer des fichiers et des dossiers peuvent potentiellement modifier leurs propres environnements ou influencer d'autres agents, créant de nouvelles voies d'attaque.

#### Vulnérabilités

*   **Injection de prompt via caractères Unicode invisibles :** Les modèles d'IA comme Gemini, Claude et Grok peuvent interpréter des points de code Unicode spécifiques (comme les `Unicode Tag codepoints`) comme des instructions exécutables. Ces caractères sont indétectables à l'œil nu dans les interfaces utilisateur standards.
    *   Un exemple concret montre l'insertion de ces caractères dans un fichier `SKILL.md` pour forcer l'IA à afficher un message spécifique ("Trust No AI") et à exécuter une commande `curl` via le tool `Bash`.
*   **Injection de prompt dans la description :** Les champs `name` et `description` d'un Skill sont chargés tôt dans le contexte du prompt système, offrant une opportunité d'injecter des instructions.
*   **Risque de chaîne d'approvisionnement :** La facilité de création et de partage de Skills, combinée à un manque de gouvernance et de contrôles de sécurité, crée un risque élevé, similaire aux malwares découverts dans des plateformes comme OpenClaw Hub.

#### Recommandations

*   **Utiliser un scanner de sécurité :** Développer ou utiliser des outils capables de détecter les caractères Unicode invisibles et les séquences potentiellement malveillantes au sein des fichiers de Skills. Un scanner simple, capable de détecter des "Unicode Tag runs" consécutifs, est mentionné.
*   **Sandboxing des agents :** Exécuter les agents dans des environnements isolés (sandboxes) en accordant des permissions explicites aux ressources et aux données. Ceci est particulièrement utile si des auto-approbations de commandes sont activées.
*   **Sélection rigoureuse des Skills :** N'installer et n'utiliser que des Skills provenant de sources et de fournisseurs de confiance.
*   **Suppression des Skills inutilisés :** Désinstaller ou supprimer les Skills qui ne sont plus nécessaires pour réduire la surface d'attaque.
*   **Prudence avec les outils sensibles :** Être particulièrement vigilant avec les Skills qui demandent l'intégration de tokens API dans des requêtes `curl` ou des opérations similaires, car cela peut entraîner des fuites ou des substitutions par des attaquants.
*   **Surveillance des mises à jour de sécurité :** Les fournisseurs d'IA travaillent à des mitigations. La détection et le refus des tags Unicode invisibles par Claude Code, observés lors des tests, indiquent des évolutions possibles dans la protection.

Il est crucial de rester attentif aux risques liés aux Skills, car leur intégration accrue dans les agents IA représente un vecteur de menaces significatif.

---
[Source](https://embracethered.com/blog/posts/2026/scary-agent-skills/){:target="_blank"}
