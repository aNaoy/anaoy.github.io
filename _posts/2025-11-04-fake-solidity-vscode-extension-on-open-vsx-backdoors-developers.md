---
title: 'Fake Solidity VSCode extension on Open VSX backdoors developers'
date: 2025-11-04
permalink: /posts/2025/11/04/fake-solidity-vscode-extension-on-open-vsx-backdoors-developers/
tags:
- veille-cyber
- bleepingcomp
---
**Une extension VS Code malveillante déguisée en outil Solidity**

Une extension malveillante nommée "juan-bianco.solidity-vlang", distribuée via le registre Open VSX, a été identifiée comme un cheval de Troie d'accès à distance, baptisé SleepyDuck. Cette extension, téléchargée plus de 53 000 fois, se fait passer pour un outil légitime pour le développement de contrats intelligents en Solidity.

Lors de sa soumission initiale le 31 octobre, l'extension était inoffensive. Cependant, une mise à jour effectuée le lendemain a introduit des fonctionnalités malveillantes.

**Points Clés :**

*   **Fonctionnalité de Rétro-persistance via Blockchain :** Le principal élément distinctif de SleepyDuck est son utilisation des contrats intelligents Ethereum pour maintenir sa persistance. Même si le serveur de commande et de contrôle (C2) principal est désactivé, le malware peut récupérer de nouvelles instructions, y compris des adresses de serveurs C2 alternatives, directement depuis la blockchain Ethereum.
*   **Activation et Exécution :** Le code malveillant s'active au démarrage de l'éditeur, lors de l'ouverture d'un fichier Solidity, ou à l'exécution de la commande de compilation Solidity. Il simule une fonction légitime ("webpack.init()") pour masquer son activité.
*   **Collecte de Données et Exécution de Commandes :** Une fois activé, SleepyDuck collecte des informations système telles que le nom d'hôte, le nom d'utilisateur, l'adresse MAC et le fuseau horaire. Il établit ensuite un environnement sécurisé pour l'exécution de commandes à distance.

**Vulnérabilités :**

Aucun numéro CVE spécifique n'est mentionné dans l'article pour cette vulnérabilité d'extension.

**Recommandations :**

*   **Prudence lors du téléchargement d'extensions :** Les développeurs doivent faire preuve de la plus grande vigilance lors du téléchargement d'extensions pour VS Code.
*   **Privilégier les sources officielles et les éditeurs réputés :** Il est conseillé de se fier uniquement aux éditeurs officiels et à leurs dépôts de confiance pour obtenir des extensions.
*   **Surveillance d'Open VSX :** L'article mentionne que le registre Open VSX a mis en place des améliorations de sécurité, notamment des durées de vie de jetons raccourcies, la révocation rapide des identifiants compromis, des analyses automatisées et le partage d'informations sur les menaces avec VS Code.

---
[Source](https://www.bleepingcomputer.com/news/security/fake-solidity-vscode-extension-on-open-vsx-backdoors-developers/){:target="_blank"}
