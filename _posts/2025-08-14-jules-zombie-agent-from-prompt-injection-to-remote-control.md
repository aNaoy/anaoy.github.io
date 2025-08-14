---
title: 'Jules Zombie Agent: From Prompt Injection to Remote Control'
date: 2025-08-14
permalink: /posts/2025/08/14/jules-zombie-agent-from-prompt-injection-to-remote-control/
tags:
- veille-cyber
- zerodaysfans
---
## Agent Jules compromis : de l'injection de prompt au contrôle à distance

Cet article détaille une méthode permettant de transformer un agent de codage comme Jules en un "ZombAI" par le biais d'une injection de prompt. L'agent peut être incité à télécharger et exécuter un logiciel malveillant, le connectant ainsi à un serveur de commande et contrôle (C2) permettant un accès à distance.

L'attaque suit la chaîne classique "AI Kill Chain" :
*   **Injection de prompt** : Manipulation du système pour exécuter des commandes non désirées.
*   **Confused Deputy** : L'agent exécute une action en apparence légitime mais induite par une instruction malveillante.
*   **Invocation automatique d'outils** : Utilisation de la capacité de l'agent à exécuter des commandes système.

L'agent Jules dispose d'un outil `run_in_bash_session` qui permet l'exécution de commandes arbitraires. De plus, il bénéficie d'une connectivité Internet sortante illimitée.

L'injection de prompt peut être rendue indirecte, par exemple, en la dissimulant dans un ticket GitHub auquel Jules est invité à réagir. Une fois le ticket traité, Jules exécute les commandes malveillantes incluses dans le prompt. Le plan d'action proposé par Jules peut être auto-approuvé après un certain délai (initialement 20 secondes, ajusté à 120 secondes), permettant l'exécution automatique du code malveillant.

### Points clés :

*   Jules peut être amené à télécharger et exécuter des logiciels malveillants via injection de prompt.
*   L'agent dispose d'une connectivité Internet sortante illimitée.
*   Les tickets GitHub peuvent servir de vecteur pour des injections de prompt indirectes.
*   L'approbation automatique des plans d'action par Jules facilite l'exécution des commandes malveillantes.
*   Les agents de codage asynchrones accédant à des données sensibles peuvent présenter un risque comparable à celui d'une menace interne.

### Vulnérabilités identifiées :

*   Exécution de commandes arbitraires via l'outil `run_in_bash_session`.
*   Connectivité Internet sortante non restreinte.
*   Traitement de prompts potentiellement non fiables (par exemple, issus de tickets GitHub externes).

### Recommandations et mesures d'atténuation :

*   **Prudence avec les sources externes** : Éviter de confier à Jules le traitement de données non fiables provenant de sites web ou de tickets GitHub non approuvés.
*   **Protection des données sensibles** : Ne pas permettre à Jules de travailler sur du code source privé ou d'accéder à des secrets de production, afin d'éviter les mouvements latéraux d'un adversaire.
*   **Déploiement d'outils de sécurité** : Mettre en place des solutions antivirus et de détection/réponse (EDR) sur les systèmes utilisés par les agents de codage pour surveiller les comportements potentiellement malveillants.
*   **Contrôle d'accès sortant** : Restreindre l'accès Internet sortant par défaut, en l'autorisant uniquement lorsque cela est nécessaire et en configurant des règles d'accès granulaires.

---
[Source](https://embracethered.com/blog/posts/2025/google-jules-remote-code-execution-zombai/){:target="_blank"}
