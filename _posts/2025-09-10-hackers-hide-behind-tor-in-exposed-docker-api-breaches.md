---
title: 'Hackers hide behind Tor in exposed Docker API breaches'
date: 2025-09-10
permalink: /posts/2025/09/10/hackers-hide-behind-tor-in-exposed-docker-api-breaches/
tags:
- veille-cyber
- bleepingcomp
---
**Menace des API Docker Exposées : Une Évolution Vers un Botnet Complexe**

Des acteurs malveillants exploitent désormais des API Docker non sécurisées en utilisant des techniques sophistiquées pour cacher leurs activités et établir des bases solides pour des botnets complexes. Initialement, ces attaques utilisaient des scripts pour déployer des cryptomineurs tout en se dissimulant via le réseau Tor.

Une évolution récente a été observée avec un nouveau type d'outil qui ne déploie pas de mineur, mais une charge utile plus avancée capable de bloquer l'accès aux API Docker compromises.

**Chaîne d'infection et capacités :**

*   Les attaquants recherchent des API Docker exposées sur le port 2375.
*   Ils envoient une requête de création de conteneur utilisant une image Alpine Linux modifiée contenant un script shell encodé en base64.
*   Ce script installe `curl` et `tor`, lance un démon Tor en arrière-plan pour masquer les communications, et utilise un proxy SOCKS5 pour vérifier la connexion.
*   Une fois Tor opérationnel, le conteneur télécharge et exécute un script de second niveau (`docker-init.sh`) depuis un service caché Tor.
*   Ce script assure la persistance en ajoutant une clé publique contrôlée par l'attaquant au fichier `authorized_keys` de l'hôte, permettant un accès SSH permanent.
*   Un cron job est configuré pour s'exécuter chaque minute, bloquant l'accès externe au port 2375 via diverses utilitaires de pare-feu disponibles (`iptables`, `nftables`, `ufw`, etc.).
*   Des outils comme `masscan`, `zstd`, `libpcap` et `torsocks` sont installés pour faciliter le scan, la propagation et l'évasion.
*   Une charge utile Go compressée (Zstandard) est téléchargée via Tor, décompressée et exécutée.
*   Cette charge utile Go agit comme un distributeur, téléchargeant et exécutant une seconde charge utile binaire et analyse le fichier `utmp` pour identifier les utilisateurs connectés.

**Comportement de construction de botnet :**

*   Le malware tente de s'auto-répliquer en scannant d'autres API Docker exposées et en les infectant via la même méthode.
*   Il supprime les conteneurs concurrents après avoir obtenu l'accès, une caractéristique typique des agents de botnets qui infectent de nouveaux nœuds de manière autonome.
*   Des logiques dormantes ont été identifiées pour exploiter Telnet (port 23) avec des identifiants par défaut de routeur et pour interagir avec l'interface de débogage à distance de Chrome (port 9222). Cela suggère des expansions futures potentielles pour le vol d'identifiants, le détournement de sessions de navigateur, le téléchargement de fichiers à distance et les attaques par déni de service distribué (DDoS).

**Vulnérabilités :**

*   L'exposition des API Docker sur le port 2375 sans authentification adéquate est la principale vulnérabilité exploitée.
*   L'utilisation de mots de passe par défaut pour les routeurs (pour les futures exploitations Telnet).
*   L'interface de débogage à distance de Chrome non sécurisée.

**Recommandations :**

*   **Sécuriser les API Docker :** Ne jamais exposer l'API Docker directement à Internet. Utiliser un accès sécurisé comme TLS ou un réseau privé virtuel (VPN).
*   **Authentification forte :** Mettre en place des mécanismes d'authentification robustes pour accéder aux services Docker.
*   **Surveillance réseau :** Surveiller activement le trafic réseau pour détecter des connexions suspectes vers ou depuis le réseau interne, en particulier sur les ports 2375.
*   **Mises à jour régulières :** Maintenir les systèmes et les conteneurs à jour avec les derniers correctifs de sécurité.
*   **Segmentation réseau :** Limiter l'accès aux API Docker aux seuls systèmes qui en ont besoin.
*   **Configuration des pare-feux :** Configurer correctement les pare-feux pour bloquer les accès non autorisés aux ports critiques.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-hide-behind-tor-in-exposed-docker-api-breaches/){:target="_blank"}
