---
title: 'The silent “Storm”: New infostealer hijacks sessions, decrypts server-side'
date: 2026-04-13
permalink: /posts/2026/04/13/the-silent-storm-new-infostealer-hijacks-sessions-decrypts-server-side/
tags:
- veille-cyber
- bleepingcomp
---
### Storm : Le nouveau malware qui contourne la sécurité par le chiffrement côté serveur

Apparu début 2026, « Storm » est un *infostealer* sophistiqué vendu sous forme d'abonnement (à partir de 900 $/mois) qui marque une évolution majeure dans le vol de données. Contrairement aux outils classiques qui déchiffrent les identifiants sur la machine infectée, Storm exfiltre les données chiffrées vers les serveurs des attaquants pour y effectuer le déchiffrement. Cette méthode permet de contourner les outils de détection d'EDR (Endpoint Detection and Response) qui surveillent généralement l'accès local aux bases de données des navigateurs.

**Points clés :**
*   **Capacités étendues :** Capture des mots de passe, cookies de session (permettant de contourner l'authentification multifacteur - MFA), données d'autocomplétion, portefeuilles crypto, et données d'applications de messagerie (Telegram, Signal, Discord).
*   **Automatisation du piratage :** Le panneau de contrôle inclut une fonction de restauration automatique des sessions via des proxies SOCKS5, facilitant l'accès immédiat aux comptes SaaS et aux environnements cloud des victimes.
*   **Infrastructure résiliente :** Les opérateurs utilisent leurs propres serveurs (VPS) pour acheminer les données volées, rendant les serveurs centraux du malware moins vulnérables aux saisies.
*   **Fonctionnement furtif :** Le malware s'exécute entièrement en mémoire pour minimiser son empreinte sur le système.

**Vulnérabilités exploitées :**
*   Le malware ne repose pas sur une CVE spécifique, mais exploite la tendance au vol de **cookies de session** (techniques de *Session Hijacking*), rendant obsolète la protection par mot de passe et neutralisant l'efficacité de la MFA.

**Recommandations :**
*   **Surveillance comportementale :** Puisque les outils traditionnels de détection d'accès local aux fichiers sont contournés, il est impératif de surveiller les anomalies de connexion (ex: accès depuis des localisations géographiques inhabituelles, comportements anormaux après authentification sur les services cloud).
*   **Protection des accès :** Appliquer le principe du moindre privilège sur les plateformes SaaS et renforcer la surveillance sur les accès aux jetons de session.
*   **Analyse réseau :** Rechercher des flux de données suspects vers des nœuds VPS inconnus, car Storm externalise le traitement des données volées.

---
[Source](https://www.bleepingcomputer.com/news/security/the-silent-storm-new-infostealer-hijacks-sessions-decrypts-server-side/){:target="_blank"}
