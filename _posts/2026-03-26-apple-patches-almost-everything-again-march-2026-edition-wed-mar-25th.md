---
title: 'Apple Patches (almost) everything again. March 2026 edition., (Wed, Mar 25th)'
date: 2026-03-26
permalink: /posts/2026/03/26/apple-patches-almost-everything-again-march-2026-edition-wed-mar-25th/
tags:
- veille-cyber
- sans-isc
---
### Mise à jour de sécurité Apple : Mars 2026

Apple a publié une importante série de correctifs corrigeant de nombreuses vulnérabilités critiques affectant l'ensemble de son écosystème. Ces failles exposent les utilisateurs à des risques d'exfiltration de données, d'élévation de privilèges, de contournement de bac à sable (sandbox) et de compromission du noyau (kernel).

#### Points clés
*   **Surface d'attaque étendue :** Les composants WebKit, le noyau (Kernel), les services de réseau (CFNetwork, SMB, NetAuth) et les frameworks de sécurité (TCC, Security) sont fortement impactés.
*   **Types de vulnérabilités :**
    *   **Accès aux données :** Un grand nombre de failles (ex: CVE-2026-20607, 20632, 20633, 20651, 20694) permettent à des applications tierces d'accéder aux données sensibles des utilisateurs.
    *   **Contournement de sécurité :** Plusieurs failles permettent de sortir de la sandbox, d'ignorer Gatekeeper (CVE-2026-20684) ou de contourner les politiques de sécurité web (CVE-2026-20643, 20665).
    *   **Privilèges :** Risques d'élévation de privilèges, y compris jusqu'au niveau root (CVE-2026-20631, 28888).
    *   **Stabilité système :** De nombreux processus peuvent être terminés de manière inattendue par des fichiers ou flux multimédias malveillants (ex: CVE-2026-20690).
*   **Vulnérabilités spécifiques :**
    *   **Activation Lock & Biométrie :** Risque de contournement du verrouillage d'activation (CVE-2025-43534) et vulnérabilité dans *App Protection* permettant d'accéder à des apps sécurisées via le code d'accès malgré la biométrie (CVE-2026-28895).
    *   **Vie privée :** Fuite de requêtes DNS via Private Relay (CVE-2025-43376) et échec de masquage de l'adresse IP dans Mail (CVE-2026-20692).

#### Vulnérabilités critiques à noter
*   **CVE-2026-20687 / 20698 / 28867 / 28868 :** Failles multiples dans le noyau (Kernel) permettant potentiellement l'écriture en mémoire, la corruption ou la divulgation d'états sensibles du système.
*   **CVE-2026-28864 :** Accès non autorisé aux éléments du Trousseau (Keychain).
*   **CVE-2026-28865 :** Interception de trafic réseau (attaque par position réseau privilégiée).

#### Recommandations
1.  **Application immédiate des correctifs :** Mettre à jour tous les appareils Apple (iOS, iPadOS, macOS, etc.) vers les versions les plus récentes incluant ces correctifs de mars 2026.
2.  **Vigilance réseau :** Étant donné les vulnérabilités liées aux partages SMB, à l'authentification réseau (NetAuth) et aux attaques de type "man-in-the-middle" (802.1X), il est conseillé de limiter la connexion aux réseaux Wi-Fi publics non sécurisés.
3.  **Gestion des accès :** Vérifier les permissions accordées aux applications tierces sur iOS et macOS, car de nombreuses failles permettent aux applications de contourner les restrictions habituelles du système.

---
[Source](https://isc.sans.edu/diary/rss/32830){:target="_blank"}
