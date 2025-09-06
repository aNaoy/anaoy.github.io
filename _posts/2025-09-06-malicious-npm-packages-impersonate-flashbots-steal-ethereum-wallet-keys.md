---
title: 'Malicious npm Packages Impersonate Flashbots, Steal Ethereum Wallet Keys'
date: 2025-09-06
permalink: /posts/2025/09/06/malicious-npm-packages-impersonate-flashbots-steal-ethereum-wallet-keys/
tags:
- veille-cyber
- hackernews
---
### Vol Malicieux dans npm : Voleurs de Clés de Portefeuilles Ethereum

Quatre paquets npm malveillants, se faisant passer pour des utilitaires cryptographiques légitimes et l'infrastructure Flashbots MEV, ont été découverts. Ils sont conçus pour dérober les clés privées et les phrases mnémoniques des développeurs Ethereum, les envoyant à un bot Telegram contrôlé par l'attaquant.

Ces paquets, mis en ligne entre septembre 2023 et août 2025 par un utilisateur nommé "flashbotts", exploitent la confiance accordée à Flashbots, une entité reconnue pour lutter contre les effets négatifs du Maximal Extractable Value (MEV) sur Ethereum.

Le paquet "@flashbotts/ethers-provider-bundle" est particulièrement insidieux. Outre sa prétendue compatibilité avec l'API Flashbots, il exfiltre des variables d'environnement via SMTP. Il est également capable de rediriger les transactions non signées vers un portefeuille contrôlé par l'attaquant et d'enregistrer des métadonnées de transactions pré-signées.

D'autres paquets comme "sdk-ethers" et "flashbot-sdk-eth" ont des fonctions conçues pour voler des phrases mnémoniques ou des clés privées lorsqu'elles sont invoquées par les développeurs. "gram-utilz" permet quant à lui l'exfiltration de données arbitraires vers le bot Telegram de l'attaquant. La présence de commentaires en vietnamien suggère une origine géographique possible pour les auteurs de ces attaques.

Ces découvertes soulignent une tentative délibérée d'exploiter la chaîne d'approvisionnement logicielle en dissimulant du code malveillant dans des utilitaires apparemment bénins, afin de contourner les analyses et de tirer parti de la confiance des développeurs. Le vol de clés privées dans cet écosystème peut entraîner la perte irréversible de fonds.

**Points Clés:**

*   Découverte de quatre paquets npm malveillants ciblant les développeurs Ethereum.
*   Imitation de l'infrastructure Flashbots pour gagner la confiance.
*   Vol de clés privées et de phrases mnémoniques vers un bot Telegram.
*   Exploitation de la chaîne d'approvisionnement logicielle via npm.
*   Potentielle origine vietnamophone des attaquants.

**Vulnérabilités:**

*   **Absence de CVE spécifique** mentionnée dans l'article, mais le vecteur d'attaque est l'injection de code malveillant dans des paquets npm.

**Recommandations:**

*   Faire preuve de prudence lors de l'installation de nouveaux paquets npm, même ceux qui semblent légitimes ou familiers.
*   Vérifier la source et la réputation des paquets avant de les intégrer dans des projets.
*   Utiliser des outils de sécurité pour l'analyse des dépendances logicielles afin de détecter des comportements suspects.
*   Sensibiliser les équipes de développement aux risques d'attaques par la chaîne d'approvisionnement logicielle.

---
[Source](https://thehackernews.com/2025/09/malicious-npm-packages-impersonate.html){:target="_blank"}
