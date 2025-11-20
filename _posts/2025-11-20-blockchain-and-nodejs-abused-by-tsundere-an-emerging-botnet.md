---
title: 'Blockchain and Node.js abused by Tsundere: an emerging botnet'
date: 2025-11-20
permalink: /posts/2025/11/20/blockchain-and-nodejs-abused-by-tsundere-an-emerging-botnet/
tags:
- veille-cyber
- securelist
---
**La Botnet Tsundere : Un Nouveau Vecteur de Menace Basé sur Node.js et la Blockchain**

Une nouvelle menace, baptisée Tsundere, est apparue, exploitant la technologie Node.js et la blockchain Ethereum pour la gestion de ses infrastructures de commande et contrôle (C2). Détectée à partir de mi-2025, elle succède à une campagne précédente de typosquatting sur npm observée en octobre 2024, ciblant notamment des bibliothèques populaires.

**Mécanismes d'Infection et Implantation :**

L'infection initiale n'est pas entièrement élucidée, mais des cas documentés impliquent l'utilisation d'outils de gestion et de surveillance à distance (RMM) téléchargeant des fichiers depuis des sites web compromis. D'autres échantillons suggèrent une diffusion par le biais de fausses versions de jeux vidéo populaires (Valorant, CS2, R6S), capitalisant sur les communautés de piratage.

Les implants Tsundere sont propagés sous deux formats :

*   **Installateur MSI :** Souvent déguisé en fausse installation de logiciels ou de jeux, cet installateur contient un ensemble de scripts et d'exécutables Node.js. Il utilise un processus d'installation Windows pour lancer un script JavaScript qui, après décryptage, déploie le bot en créant un environnement Node.js et en installant des modules essentiels (`ws`, `ethers`, `pm2`). L'utilisation de `pm2` assure la persistance et le lancement automatique du bot au démarrage.
*   **Script PowerShell :** Une méthode plus simplifiée télécharge et extrait une version officielle de Node.js. Ensuite, elle déchiffre et écrit sur le disque le script du bot et un script de persistance, utilisant également les modules `ws` et `ethers`. La persistance est assurée par une clé de registre Windows (`HKCU:\Software\Microsoft\Windows\CurrentVersion\Run`) qui lance le bot à chaque connexion.

**Infrastructure de Commande et Contrôle (C2) :**

La particularité de Tsundere réside dans son utilisation de la blockchain Ethereum pour héberger les adresses de ses serveurs C2. Un contrat intelligent (`0xa1b40044EBc2794f207D45143Bd82a1B86156c6b`) associé à un portefeuille spécifique (`0x73625B6cdFECC81A4899D221C732E1f73e504a32`) permet de stocker et de modifier dynamiquement l'adresse du serveur C2 WebSocket via la fonction `setString`. Les bots interrogent des points d'accès RPC publics pour lire cette adresse depuis la blockchain.

La communication s'établit via WebSocket après vérification de la localisation géographique de la machine cible (évitant la région CIS). Une fois connectés, le bot et le serveur échangent une clé AES et un nonce pour chiffrer toutes les communications ultérieures. Le bot transmet des informations sur le système (MAC, mémoire, GPU) pour générer un identifiant unique. Les messages de "keep-alive" (ping/pong) maintiennent la connexion. L'absence d'authentification supplémentaire rend possible la connexion de faux clients.

**Fonctionnalités et Modèle Économique :**

Le bot Tsundere est conçu pour exécuter dynamiquement du code JavaScript reçu du serveur C2 (`ID=1`). Ce code est évalué et exécuté, ses résultats étant renvoyés au serveur. Cette flexibilité permet aux opérateurs de la botnet d'adapter ses actions.

La botnet dispose d'un panneau de contrôle ("Tsundere Netto") avec un système d'inscription ouvert, proposant un marché où les utilisateurs peuvent promouvoir leurs bots et offrir divers services. Les fonctionnalités incluent la gestion des bots, des paramètres, la création de nouvelles instances de bot (MSI/PowerShell), un marché pour proposer des fonctionnalités spécifiques, un portefeuille Monero et des services de proxy SOCKS. Chaque construction génère un identifiant unique lié à l'opérateur.

**Attribution et Implications :**

Les implants contiennent des indications linguistiques (russe) pointant vers un acteur malveillant russophone. Tsundere semble lié au groupe "koneko", également impliqué dans la distribution du logiciel malveillant "123 Stealer", partageant ainsi une partie de son infrastructure. Koneko, précédemment actif sur des forums clandestins, se présentait comme un expert en malwares Node.js.

**Points Clés :**

*   **Technologie :** Node.js, Blockchain Ethereum (contrats intelligents), WebSockets.
*   **Méthodes d'Infection :** Faux installateurs (jeux/logiciels), RMM, typosquatting (précédemment).
*   **Persistance :** Clé de registre Windows, outil de gestion de processus Node.js (`pm2`).
*   **C2 :** Adresses stockées dans des contrats intelligents Ethereum, récupérées via RPC.
*   **Communication :** Chiffrée via AES, utilisant WebSockets.
*   **Fonctionnalités :** Exécution de code dynamique, marché de services de botnet.
*   **Attribution :** Acteur russophone (koneko), liens avec 123 Stealer.

**Vulnérabilités / Points d'Attention :**

Bien que l'article ne mentionne pas explicitement de CVE, les vulnérabilités exploitées se situent au niveau de :

*   **Ingénierie Sociale :** L'attrait pour les jeux et les logiciels populaires est utilisé pour tromper les utilisateurs.
*   **Gestion des Dépendances :** Les attaques par typosquatting sur npm exploitent la confiance des développeurs dans les dépôts de paquets.
*   **Configuration C2 :** L'utilisation d'une blockchain pour le C2 rend la détection et le blocage des adresses C2 plus complexes et dynamiques.
*   **Exécution de Code Dynamique :** La capacité du bot à exécuter du code arbitraire reçu du C2 est une vulnérabilité majeure permettant des actions imprévues.

**Recommandations :**

*   **Surveillance des réseaux :** Monitorer le trafic réseau pour détecter les connexions WebSocket suspectes vers des adresses IP ou des domaines inconnus.
*   **Sécurité des terminaux :** Utiliser des solutions de sécurité endpoint à jour capables de détecter les implants MSI, PowerShell et les exécutables Node.js malveillants.
*   **Gestion des dépendances :** Examiner attentivement les dépendances des projets et se méfier des paquets provenant de sources non fiables ou portant des noms suspects.
*   **Mises à jour :** Maintenir les systèmes d'exploitation, les applications et les runtimes (comme Node.js) à jour pour corriger les vulnérabilités connues.
*   **Sensibilisation des utilisateurs :** Former les utilisateurs à reconnaître les tentatives de phishing et à se méfier des téléchargements provenant de sources non officielles.
*   **Surveillance de la blockchain :** Pour les organisations particulièrement exposées, des outils de surveillance de la blockchain pourraient aider à détecter les mises à jour d'adresses C2.

---
[Source](https://securelist.com/tsundere-node-js-botnet-uses-ethereum-blockchain/117979/){:target="_blank"}
