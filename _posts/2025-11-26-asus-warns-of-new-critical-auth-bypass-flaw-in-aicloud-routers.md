---
title: 'ASUS warns of new critical auth bypass flaw in AiCloud routers'
date: 2025-11-26
permalink: /posts/2025/11/26/asus-warns-of-new-critical-auth-bypass-flaw-in-aicloud-routers/
tags:
- veille-cyber
- bleepingcomp
---
**Faille critique sur les routeurs ASUS : Contournement d'authentification via AiCloud**

ASUS a publié une mise à jour de firmware pour corriger neuf vulnérabilités de sécurité, dont une faille critique de contournement d'authentification affectant les routeurs équipés de la fonction AiCloud.

**Points Clés :**

*   La fonction AiCloud permet d'accéder à distance aux routeurs ASUS comme des serveurs cloud privés.
*   La vulnérabilité principale, CVE-2025-59366, est causée par un effet secondaire de la fonctionnalité Samba, permettant l'exécution de fonctions sans autorisation adéquate.
*   Des attaquants distants non privilégiés peuvent exploiter cette faille via des attaques à faible complexité combinant la traversée de répertoire et l'injection de commandes système, sans interaction utilisateur.

**Vulnérabilités :**

*   **CVE-2025-59366** : Contournement d'authentification critique via Samba, potentiellement déclenchable par une traversée de répertoire et une injection de commande système.
*   D'autres vulnérabilités mentionnées avec les CVE suivantes : CVE-2025-59365, CVE-2025-59368, CVE-2025-59369, CVE-2025-59370, CVE-2025-59371, CVE-2025-59372, CVE-2025-12003.
*   Une faille antérieure, **CVE-2025-2492**, avait également affecté les routeurs avec AiCloud et avait été exploitée dans le cadre de l'opération WrtHug ciblant des appareils obsolètes.

**Recommandations :**

*   **Mise à jour immédiate du firmware** : ASUS recommande fortement aux utilisateurs de mettre à jour leur firmware vers la dernière version disponible pour les séries 3.0.0.4\_386, 3.0.0.4\_388 et 3.0.0.6\_102.
*   **Mesures de mitigation pour les appareils obsolètes** :
    *   Désactiver tous les services accessibles depuis Internet (accès distant WAN, redirection de ports, DDNS, serveur VPN, DMZ, port triggering, FTP).
    *   Couper l'accès distant aux appareils utilisant la fonction AiCloud vulnérable.
*   **Sécurisation générale** :
    *   Utiliser des mots de passe forts pour la page d'administration du routeur et les réseaux sans fil.

---
[Source](https://www.bleepingcomputer.com/news/security/asus-warns-of-new-critical-auth-bypass-flaw-in-aicloud-routers/){:target="_blank"}
