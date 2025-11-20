---
title: 'Tsundere Botnet Expands Using Game Lures and Ethereum-Based C2 on Windows'
date: 2025-11-20
permalink: /posts/2025/11/20/tsundere-botnet-expands-using-game-lures-and-ethereum-based-c2-on-windows/
tags:
- veille-cyber
- hackernews
---
### Botnet Tsundere : Menace Evolutive et Utilisation de la Blockchain

Une botnet nommée Tsundere, active depuis mi-2025, cible activement les utilisateurs de Windows. Sa particularité réside dans sa capacité à exécuter du code JavaScript arbitraire récupéré depuis un serveur de commande et de contrôle (C2).

L'infection semble se propager via des leurres liés à des jeux populaires tels que Valorant, Rainbow Six Siege et Counter-Strike 2, visant potentiellement les utilisateurs à la recherche de versions piratées. L'installation se fait via un faux fichier MSI téléchargeable sur des sites compromis, utilisant un outil RMM légitime comme intermédiaire. Ce fichier installe Node.js et un script de chargement qui déchiffre et exécute la charge utile principale. Il télécharge également trois bibliothèques légitimes : ws, ethers et pm2, cette dernière assurant la persistance du bot en s'écrivant dans le registre et en se configurant pour redémarrer au démarrage du système.

Une variante utilisant des scripts PowerShell suit une démarche similaire, déployant Node.js et téléchargeant les dépendances ws et ethers, mais sans utiliser pm2. Elle garantit la persistance en créant une clé de registre pour exécuter le bot à chaque connexion.

La botnet Tsundere innove en exploitant la blockchain Ethereum pour récupérer les détails de son serveur C2 WebSocket. Ceci, via un contrat intelligent, permet aux attaquants de faire pivoter leur infrastructure de manière résiliente. Une fois l'adresse C2 récupérée, le bot établit une connexion WebSocket et reçoit du code JavaScript. Sa capacité d'évaluation de code offre flexibilité et dynamisme aux administrateurs.

Un panneau de contrôle facilite la création de nouveaux artefacts (MSI ou PowerShell), la gestion des fonctions administratives, le suivi du nombre de bots, leur utilisation comme proxy, et même la vente de botnets sur un marché dédié.

Les auteurs de Tsundere sont inconnus, mais la présence de russe dans le code source suggère un groupe russophone. Des recoupements fonctionnels existent avec une campagne malveillante npm documentée en novembre 2024. Le même serveur C2 est associé à un voleur d'informations, "123 Stealer", disponible par abonnement. L'interdiction de cibler la Russie et les pays de la CEI renforce l'hypothèse d'origines russes.

Les infections peuvent survenir via des fichiers MSI et PowerShell, permettant des déguisements, des attaques par hameçonnage ou l'intégration dans d'autres mécanismes d'attaque.

**Points Clés :**
*   Extension active de la botnet Tsundere sur Windows.
*   Utilisation de leurres de jeux pour la propagation.
*   Installation via de faux fichiers MSI et scripts PowerShell.
*   Exploitation de Node.js et de bibliothèques légitimes (ws, ethers, pm2).
*   Utilisation de la blockchain Ethereum et de contrats intelligents pour la gestion des serveurs C2.
*   Capacité d'évaluation de code JavaScript pour une flexibilité d'action.
*   Panneau de contrôle pour la gestion, la création d'artefacts et la vente de botnets.
*   Indices de liens avec des campagnes malveillantes russophones et des informations sur des voleurs d'informations.

**Vulnérabilités :**
*   Aucune vulnérabilité CVE spécifique n'est mentionnée directement pour l'exploitation du système d'exploitation dans cet article. L'infection se fait par l'exécution de fichiers malveillants (MSI, scripts PowerShell) qui exploitent les autorisations de l'utilisateur et les fonctionnalités du système.

**Recommandations :**
*   Faire preuve de prudence lors du téléchargement et de l'exécution de fichiers provenant de sources non fiables, en particulier ceux liés à des jeux ou à des logiciels piratés.
*   Mettre à jour régulièrement le système d'exploitation Windows et les logiciels pour corriger les vulnérabilités connues.
*   Utiliser une solution antivirus et anti-malware fiable et la maintenir à jour.
*   Être vigilant face aux tentatives de phishing ou aux e-mails suspects.
*   Vérifier la légitimité des outils et des scripts exécutés sur le système.

---
[Source](https://thehackernews.com/2025/11/tsundere-botnet-expands-using-game.html){:target="_blank"}
