---
title: '22 Seconds to Compromise: How Automated SSH Actors Move From Login to Persistence Before You Can Blink &#x5b;Guest Diary&#x5d;, (Thu, Aug 6th)'
date: 2026-08-06
permalink: /posts/2026/08/06/22-seconds-to-compromise-how-automated-ssh-actors-move-from-login-to-persistence-before-you-can-blink-x5bguest-diaryx5d-thu-aug-6th/
tags:
- veille-cyber
- sans-isc
---
### Compromission SSH automatisée : La menace en 22 secondes

Une étude réalisée via un pot de miel (honeypot) Cowrie démontre une campagne persistante d'attaques SSH automatisées capables de compromettre un système en seulement 22 secondes. Dès l'authentification réussie, un script exécute une série d'actions pré-programmées pour installer une porte dérobée, verrouiller les administrateurs légitimes et effacer les traces de restriction.

**Points clés :**
*   **Rapidité extrême :** Le processus d'exploitation est entièrement automatisé, ne laissant aucune chance à une intervention humaine manuelle.
*   **Infrastructure coordonnée :** Les attaques proviennent de botnets ou de réseaux distribués (ex: campagne « mdrfckr ») scannant l'Internet en continu.
*   **Cibles généralistes :** L'attaque ne vise pas une entité spécifique, mais cherche systématiquement les systèmes mal configurés utilisant des mots de passe faibles.
*   **Techniques observées (MITRE ATT&CK) :**
    *   T1078 : Utilisation de comptes valides (brute force).
    *   T1098 : Manipulation de compte (injection de clés SSH).
    *   T1059 : Exécution de commandes automatisées.
    *   T1562 : Altération des défenses (suppression de `/etc/hosts.deny`).

**Vulnérabilités :**
*   **CVE-N/A :** Il ne s'agit pas d'une vulnérabilité logicielle (Zero-day), mais d'une exploitation de **configurations faibles** (mots de passe devinables et authentification par mot de passe activée sur SSH).

**Recommandations :**
*   **Désactiver l'authentification par mot de passe :** Privilégier exclusivement l'authentification par clés SSH (M1042).
*   **Renforcer les politiques de mots de passe :** Supprimer les mots de passe par défaut et imposer une complexité stricte (M1027).
*   **Limiter l'exposition réseau :** Restreindre l'accès SSH aux adresses IP de confiance ou via VPN (M1030).
*   **Automatiser la défense :** Utiliser des outils comme `fail2ban` pour bannir les IP après plusieurs tentatives infructueuses (M1036).
*   **Audit et Monitoring :** Surveiller les logs d'authentification en temps réel pour détecter les séquences de commandes suspectes survenant immédiatement après une connexion.

---
[Source](https://isc.sans.edu/diary/rss/33220){:target="_blank"}
