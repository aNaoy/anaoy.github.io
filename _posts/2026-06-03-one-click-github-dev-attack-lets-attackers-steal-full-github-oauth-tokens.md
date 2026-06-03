---
title: 'One-Click GitHub Dev Attack Lets Attackers Steal Full GitHub OAuth Tokens'
date: 2026-06-03
permalink: /posts/2026/06/03/one-click-github-dev-attack-lets-attackers-steal-full-github-oauth-tokens/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans GitHub.dev : Vol de jetons OAuth via VS Code

Une faille de sécurité dans l'environnement GitHub.dev permet à des attaquants de dérober les jetons d'accès OAuth des utilisateurs par le simple clic sur un lien malveillant. Ce jeton, utilisé pour permettre l'interaction entre GitHub.com et l'éditeur web GitHub.dev, dispose de droits étendus permettant la lecture et l'écriture sur l'intégralité des dépôts, y compris privés.

**Points clés :**
*   **Mécanisme d'attaque :** L'attaque exploite le système de messagerie entre la fenêtre principale de VS Code et les *webviews* (utilisées pour le rendu Markdown ou les notebooks).
*   **Exécution :** Un script JavaScript malveillant injecté dans une *webview* simule des frappes clavier pour ouvrir la palette de commandes et installer silencieusement une extension malveillante.
*   **Contournement de sécurité :** L'attaquant utilise la fonctionnalité des "extensions d'espace de travail local" (*local workspace extensions*), qui permet d'installer une extension sans invite de confiance si celle-ci est située dans le dossier `.vscode/extensions` du projet.
*   **Portée :** La vulnérabilité est spécifique à l'environnement web GitHub.dev et ne concerne pas l'application VS Code de bureau.

**Vulnérabilités :**
*   Aucun identifiant CVE n'a été attribué à ce jour. La faille repose sur une combinaison d'abus de fonctionnalités légitimes (manipulation de *webviews* et installation d'extensions locales).

**Recommandations :**
*   **Vigilance accrue :** Évitez de cliquer sur des liens suspects pointant vers des dépôts GitHub inconnus ou des environnements GitHub.dev non vérifiés.
*   **Surveillance :** Soyez prudent lors de l'ouverture de projets contenant un dossier `.vscode` suspect ou non familier.
*   **Attente d'un correctif :** Microsoft a reconnu le problème et travaille actuellement sur un correctif pour limiter les risques liés aux *webviews* et aux extensions locales dans GitHub.dev.

---
[Source](https://thehackernews.com/2026/06/one-click-github-dev-attack-lets.html){:target="_blank"}
