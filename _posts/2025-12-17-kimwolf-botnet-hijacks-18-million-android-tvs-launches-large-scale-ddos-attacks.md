---
title: 'Kimwolf Botnet Hijacks 1.8 Million Android TVs, Launches Large-Scale DDoS Attacks'
date: 2025-12-17
permalink: /posts/2025/12/17/kimwolf-botnet-hijacks-18-million-android-tvs-launches-large-scale-ddos-attacks/
tags:
- veille-cyber
- hackernews
---
## Botnet Kimwolf : 1.8 Millions de Télévisions Android Compromises pour des Attaques DDoS

Une nouvelle botnet de type "distributed denial-of-service" (DDoS), nommée Kimwolf, a infecté environ 1,8 million d'appareils Android, principalement des télévisions et des boîtiers TV. Ces appareils sont utilisés pour lancer des attaques DDoS à grande échelle. Il est suspecté que Kimwolf soit lié à la botnet AISURU, responsable de plusieurs attaques DDoS record.

Les chercheurs ont identifié que Kimwolf utilise le NDK (Native Development Kit) d'Android et offre des fonctionnalités avancées au-delà des attaques DDoS, incluant le proxy forwarding, le reverse shell et la gestion de fichiers. Entre le 19 et le 22 novembre 2025, la botnet aurait émis 1,7 milliard de commandes d'attaque DDoS.

Les appareils ciblés sont variés, incluant des modèles comme TV BOX, SuperBOX, HiDPTAndroid, P200, X96Q, XBOX, SmartTV et MX10. Les infections sont réparties mondialement, avec des concentrations notables au Brésil, en Inde, aux États-Unis, en Argentine, en Afrique du Sud et aux Philippines. La méthode de propagation exacte n'est pas encore claire.

La botnet a démontré une capacité d'adaptation notable, ayant recours au service ENS (Ethereum Name Service) pour masquer ses serveurs de commande et contrôle (C2) suite à plusieurs interruptions de ses domaines C2 par des tiers inconnus.

**Points clés :**

*   **Nature de la menace :** Botnet DDoS massive ciblant les appareils Android TV.
*   **Échelle :** 1,8 million d'appareils infectés.
*   **Fonctionnalités :** Attaques DDoS, proxy forwarding, reverse shell, gestion de fichiers.
*   **Association :** Lien suspecté avec la botnet AISURU, appartenant potentiellement au même groupe d'attaquants.
*   **Méthodes d'évasion :** Utilisation d'ENS pour masquer l'infrastructure C2.
*   **Objectifs des attaques :** Principalement des entités basées aux États-Unis, en Chine, en France, en Allemagne et au Canada.
*   **Utilisation des nœuds :** Plus de 96% des commandes visent à utiliser les appareils compromis comme services proxy, suggérant une exploitation de bande passante pour un profit maximal.

**Vulnérabilités exploitées :**

L'article ne détaille pas de vulnérabilités spécifiques avec des identifiants CVE. Cependant, l'infection des appareils suggère l'exploitation de failles permettant l'exécution de code à distance ou l'accès non autorisé, potentiellement via des applications malveillantes, des firmwares compromis, ou des faiblesses dans les configurations réseau des appareils.

**Recommandations :**

Bien que l'article ne fournisse pas de recommandations directes, les observations sur Kimwolf impliquent les mesures suivantes :

*   **Sécurisation des appareils :** Il est crucial de s'assurer que les télévisions Android, les boîtiers TV et autres appareils connectés sont maintenus à jour avec les derniers correctifs de sécurité.
*   **Surveillance du réseau :** Les utilisateurs devraient surveiller leur trafic réseau pour détecter des activités suspectes provenant de leurs appareils connectés.
*   **Authentification forte :** L'utilisation de mots de passe forts et uniques pour les comptes associés à ces appareils et pour l'accès Wi-Fi peut limiter la surface d'attaque.
*   **Vigilance face aux applications :** Être prudent quant aux applications installées sur les appareils Android TV et privilégier les sources fiables.
*   **Recherche par les fabricants :** Les fabricants d'appareils devraient renforcer la sécurité de leurs produits et implémenter des mécanismes de mise à jour de sécurité robustes.

---
[Source](https://thehackernews.com/2025/12/kimwolf-botnet-hijacks-18-million.html){:target="_blank"}
