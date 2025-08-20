---
title: 'Amazon Q Developer for VS Code Vulnerable to Invisible Prompt Injection'
date: 2025-08-20
permalink: /posts/2025/08/20/amazon-q-developer-for-vs-code-vulnerable-to-invisible-prompt-injection/
tags:
- veille-cyber
- zerodaysfans
---
**Amazon Q Developer VS Code : Injection Invisible et Exécution de Code à Distance**

L'extension Amazon Q Developer pour VS Code, très populaire, présentait une vulnérabilité permettant des attaques par injection de prompt invisibles. Ces attaques exploitaient des caractères Unicode non affichables, interprétés par le modèle d'IA comme des instructions. Cela pouvait mener à l'exfiltration de données sensibles ou à l'exécution de code arbitraire sur la machine de l'utilisateur. Le problème réside dans la manière dont les modèles Anthropic Claude, utilisés par Amazon Q, traitent ces caractères spéciaux.

**Points Clés :**

*   **Injection de Prompt Invisible :** Des caractères Unicode non visibles peuvent être intégrés dans des fichiers pour dicter des actions à l'IA, contournant la surveillance humaine.
*   **Exécution de Code :** Associée à des exploits comme `find -exec`, cette vulnérabilité permettait l'exécution de commandes arbitraires.
*   **Vulnérabilité des Modèles :** Les modèles Anthropic Claude sont connus pour interpréter ces caractères comme des instructions, une faiblesse non corrigée au niveau du modèle par Anthropic.
*   **Responsabilité des Développeurs :** Il incombe aux développeurs d'applications comme Amazon Q de mettre en place des mesures de sécurité.

**Vulnérabilités :**

*   Injection de prompt via caractères Unicode invisibles (non spécifié CVE).
*   Exécution de code à distance via injection indirecte de prompt (non spécifié CVE).

**Recommandations :**

*   Supprimer ou neutraliser les caractères Unicode problématiques avant le traitement des entrées.
*   Implémenter des mesures de sécurité visuelles et techniques, comme la validation par un humain.
*   Inclure la détection automatisée des utilisations suspectes d'Unicode dans les systèmes de surveillance.
*   Corriger la vulnérabilité d'exécution de code à distance par injection indirecte.

La vulnérabilité a été corrigée par AWS, mais aucun avis public ni CVE n'ont été émis. Il est recommandé de maintenir l'extension à jour.

---
[Source](https://embracethered.com/blog/posts/2025/amazon-q-developer-interprets-hidden-instructions/){:target="_blank"}
