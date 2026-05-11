---
title: 'Instructure confirms hackers used Canvas flaw to deface portals'
date: 2026-05-11
permalink: /posts/2026/05/11/instructure-confirms-hackers-used-canvas-flaw-to-deface-portals/
tags:
- veille-cyber
- bleepingcomp
---
### Violation de Canvas par le groupe ShinyHunters : extorsion et fuite de données

L'entreprise Instructure a subi une double cyberattaque visant sa plateforme d'apprentissage Canvas. Après une intrusion initiale ayant conduit à l'exfiltration de 3,6 To de données, les attaquants (le groupe ShinyHunters) ont exploité une faille de type XSS pour défigurer les portails de connexion et exercer une pression à l'extorsion.

**Points clés :**
*   **Impact massif :** Plus de 8 800 établissements d'enseignement touchés et environ 275 millions d'enregistrements (noms d'utilisateurs, adresses email, informations de cours) potentiellement compromis.
*   **Mode opératoire :** Les attaquants ont utilisé des vulnérabilités Cross-Site Scripting (XSS) via les fonctionnalités de contenu généré par les utilisateurs pour détourner des sessions d'administrateurs authentifiés.
*   **Mesures d'urgence :** Instructure a temporairement mis hors ligne la version « Free-for-Teacher » de sa plateforme et a révoqué les accès suspects pour stopper la campagne de défiguration.

**Vulnérabilités :**
*   **Type :** Multiples failles XSS (Cross-Site Scripting). 
*   **CVE :** Aucune CVE spécifique n'a été communiquée à ce stade par l'éditeur.

**Recommandations :**
*   **Pour les utilisateurs :** Restez vigilants face aux tentatives de phishing liées à vos identifiants académiques. Un changement de mot de passe est recommandé par mesure de prudence.
*   **Pour les administrateurs de plateformes :**
    *   Renforcer la sécurisation des fonctionnalités permettant l'intégration de contenu généré par les utilisateurs.
    *   Mettre en œuvre une politique stricte de Content Security Policy (CSP) pour limiter l'exécution de scripts non autorisés.
    *   Appliquer systématiquement les correctifs de sécurité fournis par l'éditeur dès leur disponibilité.
    *   Auditer régulièrement les permissions des sessions administrateur.

---
[Source](https://www.bleepingcomputer.com/news/security/instructure-confirms-hackers-used-canvas-flaw-to-deface-portals/){:target="_blank"}
