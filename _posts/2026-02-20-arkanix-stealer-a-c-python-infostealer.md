---
title: 'Arkanix Stealer: a C++ & Python infostealer'
date: 2026-02-20
permalink: /posts/2026/02/20/arkanix-stealer-a-c-python-infostealer/
tags:
- veille-cyber
- securelist
---
## Arkanix Stealer : un logiciel malveillant dérobant des informations

Début octobre 2025, une nouvelle menace baptisée "Arkanix Stealer" a été identifiée. Opérant sous un modèle de "malware-as-a-service" (MaaS), elle proposait non seulement le logiciel espion mais aussi un panneau de contrôle pour gérer les charges utiles et visualiser les statistiques. La campagne semble avoir été de courte durée, le programme d'affiliation ayant été rapidement désactivé.

### Points clés

*   **Modèle MaaS :** Arkanix Stealer était proposé comme un service, facilitant son acquisition et son utilisation par des acteurs malveillants.
*   **Double implémentation :** Le logiciel malveillant existait en deux versions : une écrite en C++ (native) et une autre en Python.
*   **Distribution via Phishing :** Les noms de fichiers de scripts de chargement suggèrent que le phishing était un vecteur d'infection probable.
*   **Fonctionnalités étendues :** Le stealer pouvait collecter une grande variété d'informations sensibles.
*   **Développement assisté par IA :** Des indices suggèrent l'utilisation d'outils d'aide au développement basés sur l'IA, potentiellement pour accélérer le processus.
*   **Campagne éphémère :** La campagne a été de courte durée, avec la désactivation du panneau de contrôle et du canal de communication Discord fin 2025.

### Vulnérabilités et Capacités d'Exploitation

Arkanix Stealer ne cible pas une vulnérabilité spécifique dans le sens traditionnel (comme une faille logicielle), mais exploite plutôt des failles de sécurité humaines (phishing) et des fonctionnalités intégrées aux systèmes et applications pour dérober des informations.

Ses capacités incluent :

*   **Collecte d'informations système :** Version de l'OS, informations CPU/GPU, RAM, résolution d'écran, disposition du clavier, fuseau horaire, logiciels installés, antivirus, VPN.
*   **Vol d'identifiants de navigateurs :** Historique de navigation, informations de remplissage automatique (e-mail, téléphone, cartes de paiement), mots de passe enregistrés, cookies. Il prend en charge 22 navigateurs, y compris Tor Browser.
*   **Détournement de données Telegram :** Collection du répertoire `tdata` ou de sous-dossiers spécifiques contenant des messages.
*   **Vol d'identifiants Discord :** Capture d'identifiants du client Discord standard et personnalisé.
*   **Auto-propagation sur Discord :** Possibilité d'envoyer des messages à la liste d'amis et aux canaux d'un utilisateur compromis.
*   **Vol d'identifiants VPN :** Recherche et extraction de credentials pour des VPN populaires comme Mullvad, NordVPN, ExpressVPN, ProtonVPN.
*   **Exfiltration de fichiers :** Recherche de documents et de fichiers médias sur le système de l'utilisateur.
*   **Vol d'informations RDP :** Collecte d'adresses de serveur RDP, de mots de passe, de noms d'utilisateur et de ports.
*   **Vol d'identifiants de plateformes de jeux :** Ciblage de Steam, Epic Games Launcher, Riot, Origin, etc.
*   **Capture d'écrans :** La version native peut capturer des captures d'écran.
*   **Injection de "ChromElevator" :** La version C++ télécharge et injecte le module ChromElevator pour voler des données de navigateurs, notamment des clés de navigateur.
*   **Patcher de portefeuilles cryptographiques :** Vérifie l'installation des portefeuilles Exodus et Atomic.
*   **Collecte supplémentaire :** D'autres modules peuvent collecter des données de FileZilla, des screenshots, etc.
*   **HVNC (Malware de réseau privé virtuel caché) :** Un module pouvant être exécuté au démarrage du système.

Aucun identifiant CVE spécifique n'est associé directement à Arkanix Stealer, car il agit en exploitant des fonctionnalités existantes et des vecteurs d'infection communs.

### Recommandations

Les mesures de sécurité suivantes sont recommandées pour se protéger contre des menaces similaires :

*   **Vigilance face au phishing :** Ne pas cliquer sur des liens suspects ou ouvrir des pièces jointes provenant d'expéditeurs inconnus ou non sollicités.
*   **Mises à jour logicielles :** Maintenir les systèmes d'exploitation, les navigateurs et tous les logiciels à jour pour corriger les vulnérabilités connues.
*   **Logiciels antivirus et antimalware :** Utiliser et maintenir à jour une solution de sécurité fiable, capable de détecter les menaces comme Arkanix Stealer (détecté sous les noms `Trojan-PSW.Win64.Coins.*`, `HEUR:Trojan-PSW.Multi.Disco.gen`, `Trojan.Python.Agent.*`).
*   **Authentification forte :** Activer l'authentification multifacteur (MFA) chaque fois que possible, en particulier pour les services critiques comme les comptes bancaires et les plateformes en ligne.
*   **Sauvegardes régulières :** Effectuer des sauvegardes régulières des données importantes pour pouvoir les restaurer en cas de compromission.
*   **Prudence avec les logiciels :** Être prudent lors du téléchargement et de l'installation de logiciels, et privilégier les sources officielles.
*   **Surveillance des transactions :** Surveiller attentivement les activités sur les comptes bancaires et les portefeuilles de cryptomonnaies.

---
[Source](https://securelist.com/arkanix-stealer/119006/){:target="_blank"}
