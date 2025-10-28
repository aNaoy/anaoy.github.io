---
title: 'ChatGPT Atlas Browser Can Be Tricked by Fake URLs into Executing Hidden Commands'
date: 2025-10-28
permalink: /posts/2025/10/28/chatgpt-atlas-browser-can-be-tricked-by-fake-urls-into-executing-hidden-commands/
tags:
- veille-cyber
- hackernews
---
### Navigation d'un navigateur IA compromise par des URLs falsifiées

Le navigateur web ChatGPT Atlas d'OpenAI est vulnérable à une attaque d'injection de prompt. Celle-ci permet à un attaquant de faire exécuter des commandes cachées à l'agent IA en falsifiant une URL. L'omnibox du navigateur, qui interprète les entrées comme des adresses ou des commandes, peut être exploité. En présentant une instruction malveillante sous une forme qui ressemble à une URL, l'attaquant trompe le navigateur pour qu'il traite l'entrée comme une "intention utilisateur" de confiance, déclenchant ainsi l'exécution de la commande cachée. Cette technique pourrait être utilisée pour rediriger les utilisateurs vers des sites de phishing, voler des données ou même supprimer des fichiers. D'autres navigateurs IA, comme Perplexity Comet et Opera Neon, ont également montré des vulnérabilités similaires, démontrant que les injections de prompt constituent un défi de sécurité majeur pour l'industrie de l'IA.

**Points Clés :**

*   Le navigateur ChatGPT Atlas peut être la cible d'une attaque d'injection de prompt via sa barre d'adresse (omnibox).
*   Les attaquants peuvent masquer des instructions malveillantes dans des chaînes de caractères ressemblant à des URLs.
*   Le navigateur interprète ces entrées falsifiées comme des commandes de confiance, déclenchant des actions indésirables.
*   Les conséquences peuvent aller de la redirection vers des sites malveillants à l'exécution de commandes dangereuses.
*   Des vulnérabilités similaires ont été observées dans d'autres navigateurs IA.

**Vulnérabilités :**

*   **Prompt Injection (injection de prompt)** : Le navigateur ne distingue pas suffisamment entre une URL légitime et une instruction malveillante déguisée en URL, traitant cette dernière comme une entrée utilisateur de confiance.
*   Absence de CVE spécifique mentionnée dans l'article pour cette vulnérabilité particulière dans ChatGPT Atlas.

**Recommandations :**

*   **Validation stricte des entrées de l'omnibox** : Renforcer la validation pour distinguer clairement les URLs valides des instructions.
*   **Isolation des entrées utilisateur et du contenu web** : Mettre en place des mécanismes de défense plus robustes pour éviter que des instructions cachées ne soient interprétées comme des commandes par l'agent IA.
*   **Surveillance et détection des comportements anormaux** : Détecter les tentatives d'exécution de commandes imprévues ou les redirections vers des sites suspects.
*   **Sensibilisation des utilisateurs** : Informer les utilisateurs sur les risques potentiels liés aux interactions avec les navigateurs IA et les URLs suspectes.
*   **Développement continu de défenses** : L'industrie de l'IA travaille activement à atténuer ces vulnérabilités par la formation des modèles, l'ajout de garde-fous et des notifications transparentes.

---
[Source](https://thehackernews.com/2025/10/chatgpt-atlas-browser-can-be-tricked-by.html){:target="_blank"}
