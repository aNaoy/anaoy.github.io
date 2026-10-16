---
title: 'Panchans Mining Island &#x5b;Guest Diary&#x5d;, (Wed, Oct 14th)'
date: 2026-10-16
permalink: /posts/2026/10/16/panchans-mining-island-x5bguest-diaryx5d-wed-oct-14th/
tags:
- veille-cyber
- sans-isc
---
### Analyse du ver de minage Panchan

**Points clés**
Le ver Panchan, identifié en 2022 et développé en langage Go, est un botnet pair-à-pair (P2P) conçu pour l'extraction de cryptomonnaies. Il se propage en exploitant les vulnérabilités des systèmes exposés sur Internet, en dérobant des clés SSH pour se déplacer latéralement et en utilisant un rootkit pour maintenir sa persistance. Une caractéristique notable de cette variante est l'utilisation de canaux Discord comme infrastructure de commande et de contrôle (C2).

**Vulnérabilités exploitées**
L'article ne mentionne pas de CVE spécifique, car le ver cible principalement des mauvaises configurations plutôt que des failles logicielles précises :
*   Services SSH mal sécurisés ou exposés publiquement (mots de passe faibles, accès root autorisé).
*   Absence de filtrage réseau (ingress/egress).
*   Clés SSH privées stockées et oubliées sur le système, facilement accessibles après infection.
*   Absence de segmentation réseau et de surveillance des journaux.

**Recommandations**
*   **Sécurité SSH :** Désactiver la connexion root, privilégier l'authentification par clé plutôt que par mot de passe, et utiliser `Fail2Ban` pour limiter les tentatives de force brute.
*   **Gestion des accès :** Mettre en place l'authentification multi-facteurs (MFA) et utiliser des listes de contrôle d'accès (ACL) ou des serveurs rebonds (jump box).
*   **Gestion des clés :** Utiliser `HashKnownHosts` pour masquer les hôtes connus et implémenter une solution comme *HashiCorp Vault* pour délivrer des certificats SSH éphémères, rendant le vol de clés caduc.
*   **Filtrage et surveillance :**
    *   Appliquer des règles strictes de filtrage entrant/sortant.
    *   Déployer un système de détection/prévention d'intrusion (IDS/IPS).
    *   Centraliser les logs dans un SIEM pour détecter les comportements anormaux (installations de logiciels suspects, élévation de privilèges, communications vers Discord).
*   **Stratégie globale :** Appliquer le principe du « refus par défaut » pour tout trafic réseau.

**Indicateurs de compromission (IoC)**
*   Multiples tentatives d'authentification SSH échouées.
*   Consommation de ressources système inhabituelle.
*   Processus persistants impossibles à terminer.
*   Présence de répertoires cachés avec des noms aléatoires (haute entropie) dans `/tmp` ou les dossiers utilisateurs.
*   Trafic réseau récurrent vers les services de messagerie Discord.

---
[Source](https://isc.sans.edu/diary/rss/33426){:target="_blank"}
