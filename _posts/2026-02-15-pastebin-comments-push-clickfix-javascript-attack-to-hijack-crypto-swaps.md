---
title: 'Pastebin comments push ClickFix JavaScript attack to hijack crypto swaps'
date: 2026-02-15
permalink: /posts/2026/02/15/pastebin-comments-push-clickfix-javascript-attack-to-hijack-crypto-swaps/
tags:
- veille-cyber
- bleepingcomp
---
**Attaque ClickFix Ciblée sur les Échanges de Cryptomonnaies via JavaScript**

Une nouvelle campagne de cyberattaque utilise des commentaires sur Pastebin pour diffuser un logiciel malveillant de type "ClickFix" visant les utilisateurs de cryptomonnaies. Les attaquants promettent un exploit d'arbitrage sur Swapzone.io, incitant les victimes à exécuter du code JavaScript dans leur navigateur. Ce code modifie discrètement le processus d'échange de cryptomonnaies, détournant les fonds vers des portefeuilles contrôlés par les pirates. Cette méthode est notable car elle semble être l'une des premières attaques ClickFix à exploiter le JavaScript directement dans le navigateur pour manipuler une page web à des fins malveillantes.

**Points Clés :**

*   **Diffusion :** Les commentaires malveillants sont postés sur Pastebin, orientant les victimes vers des liens hébergés sur rawtext[.]host.
*   **Ingénierie Sociale :** La tromperie repose sur une fausse promesse de profits importants grâce à un exploit d'arbitrage sur Swapzone.io, décrite dans un document Google Docs.
*   **Mécanisme d'Attaque :** Les victimes sont instruites à exécuter un script JavaScript via l'URI `javascript:` dans la barre d'adresse de leur navigateur lorsqu'elles sont sur le site Swapzone.io.
*   **Manipulation de l'Interface :** Le script injecté modifie le processus d'échange, remplaçant les adresses de dépôt légitimes par celles des attaquants. Il falsifie également les taux de change affichés pour renforcer la crédibilité de l'exploit.
*   **Nature de l'Attaque :** Il s'agit d'une variante de l'attaque ClickFix, qui détourne généralement les utilisateurs vers l'exécution de commandes système. Ici, le ciblage se fait au niveau du navigateur via JavaScript.
*   **Irréversibilité :** Les transactions Bitcoin étant irréversibles, les fonds envoyés aux adresses malveillantes sont perdus.

**Vulnérabilités Exploités :**

*   **Ingénierie Sociale :** Exploitation de la confiance et de la recherche de profits rapides des utilisateurs.
*   **Abus de l'URI `javascript:` :** Permet l'exécution de code JavaScript directement dans le contexte du navigateur de la victime.
*   **Injection de Scripts :** Remplacement des scripts légitimes de la page par du code malveillant pour intercepter et modifier les données de transaction.

**Recommandations :**

*   **Prudence avec les Liens Suspects :** Éviter de cliquer sur des liens provenant de sources non fiables ou promettant des gains irréalistes.
*   **Méfiance envers les Instructions Inhabituelles :** Ne jamais exécuter de code JavaScript en copiant/collant des extraits dans la barre d'adresse du navigateur, surtout sur des sites financiers.
*   **Vérification des Adresses :** Toujours vérifier attentivement les adresses de portefeuille avant d'envoyer des fonds lors d'un échange de cryptomonnaies.
*   **Sensibilisation :** Informer les utilisateurs sur les tactiques d'ingénierie sociale courantes et les risques liés aux manipulations de navigateur.

---
[Source](https://www.bleepingcomputer.com/news/security/pastebin-comments-push-clickfix-javascript-attack-to-hijack-crypto-swaps/){:target="_blank"}
