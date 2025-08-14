---
title: 'Leak: OpenAIs browser will use ChatGPT Agent to control the browser'
date: 2025-08-14
permalink: /posts/2025/08/14/leak-openais-browser-will-use-chatgpt-agent-to-control-the-browser/
tags:
- veille-cyber
- bleepingcomp
---
**L'Agent ChatGPT prend le contrôle du navigateur OpenAI**

OpenAI développe un navigateur basé sur Chromium qui intégrera une fonctionnalité "Agent" alimentée par ChatGPT. Actuellement, le mode Agent de ChatGPT permet de naviguer sur le web via une machine virtuelle Linux dans le cloud, mais sans contrôle direct du navigateur de l'utilisateur ni accès aux onglets ou autres fonctionnalités de navigation.

Les récentes découvertes indiquent que le mode Agent pourrait bientôt avoir deux options d'exécution : un navigateur cloud virtuel ou le nouveau navigateur local d'OpenAI. Un indicateur caché et une chaîne d'agent utilisateur ("ChatGPT...Macintosh;...Chrome") suggèrent que cette fonctionnalité sera activée sur l'application ou le navigateur d'OpenAI pour Mac, le navigateur cloud servant de solution de repli.

Des rapports antérieurs et la documentation d'OpenAI confirment que les agents utilisent des captures d'écran d'une fenêtre de navigateur virtuelle pour interagir avec les sites web, telles que cliquer et remplir des formulaires. Reuters a également rapporté qu'OpenAI prévoit de lancer son propre navigateur basé sur Chromium afin de centraliser davantage les interactions au sein d'une interface de type ChatGPT.

**Points clés :**

*   OpenAI développe un navigateur basé sur Chromium.
*   Ce navigateur intégrera une fonctionnalité "Agent" contrôlée par ChatGPT.
*   Le mode Agent actuel utilise une machine virtuelle dans le cloud pour naviguer.
*   La nouvelle version permettra potentiellement au mode Agent de contrôler directement un navigateur local.

**Vulnérabilités potentielles :**

Bien que l'article ne mentionne pas de CVE spécifiques, l'intégration accrue d'un agent IA capable de contrôler un navigateur soulève des préoccupations potentielles en matière de sécurité, notamment :

*   **Risques d'exécution de code malveillant :** Si un agent malveillant parvient à prendre le contrôle du navigateur, il pourrait potentiellement exécuter du code arbitraire sur le système de l'utilisateur.
*   **Collecte et exposition de données sensibles :** La capacité d'un agent à naviguer et interagir avec des sites pourrait entraîner la collecte non autorisée d'informations personnelles ou sensibles si l'agent est compromis ou mal conçu.
*   **Usurpation d'identité et attaques de phishing :** Un agent pourrait être manipulé pour effectuer des actions au nom de l'utilisateur sur des sites web, ouvrant la porte à des tentatives d'usurpation d'identité ou à des attaques de phishing avancées.

**Recommandations :**

*   **Vigilance lors de l'utilisation de la fonction Agent :** Les utilisateurs doivent être conscients des capacités du mode Agent et de la nécessité de le faire fonctionner dans un environnement sécurisé.
*   **Mises à jour de sécurité régulières :** Il est crucial de maintenir le navigateur OpenAI et les composants associés à jour pour bénéficier des derniers correctifs de sécurité.
*   **Autorisations granulaires :** OpenAI devrait envisager de fournir des contrôles d'autorisation granulaires pour le mode Agent, permettant aux utilisateurs de limiter ses actions et l'accès aux données.
*   **Audit de sécurité approfondi :** Avant le lancement, une évaluation de sécurité rigoureuse du navigateur et de son intégration avec l'agent ChatGPT est essentielle pour identifier et atténuer les vulnérabilités potentielles.

---
[Source](https://www.bleepingcomputer.com/news/artificial-intelligence/leak-openais-browser-will-use-chatgpt-agent-to-control-the-browser/){:target="_blank"}
