---
title: 'EDR, Email, and SASE Miss This Entire Class of Browser Attacks'
date: 2026-02-06
permalink: /posts/2026/02/06/edr-email-and-sase-miss-this-entire-class-of-browser-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Les Attaques Ciblant le Navigateur : Un Angle Mort pour les Défenses Actuelles

Le travail en entreprise s'effectue désormais majoritairement via le navigateur web. Cependant, les architectures de sécurité existantes (EDR, sécurité email, SASE) se concentrent sur les points d'accès périphériques et peinent à observer les activités internes au navigateur. Cette lacune crée un "refuge" pour les attaquants qui exploitent des techniques laissant peu de traces traditionnelles.

#### Types d'attaques courantes ciblant le navigateur :

*   **ClickFix et Ingénierie Sociale Guidée par l'Interface Utilisateur :** Des messages frauduleux dans le navigateur incitent l'utilisateur à copier, coller ou soumettre des informations sensibles. Aucune charge utile ni exploit n'est utilisé, rendant l'investigation difficile.
*   **Extensions Malveillantes :** Des extensions apparemment légitimes sont installées pour surveiller le contenu des pages, intercepter les saisies ou exfiltrer des données, sans déclencher d'alertes au niveau de l'endpoint ou du réseau.
*   **Attaques "Man-in-the-Browser" (et variantes) :** Ces attaques détournent des sessions de navigateur valides. Les identifiants sont corrects, l'authentification multifacteur est validée, et l'activité semble légitime, rendant difficile la distinction entre une session manipulée et une session authentique.
*   **HTML Smuggling :** Le contenu malveillant est assemblé dans le navigateur via JavaScript, contournant les mécanismes de téléchargement et d'inspection traditionnels.

#### Pourquoi les outils actuels échouent :

Les systèmes EDR, de sécurité email et SASE sont conçus pour analyser les processus, les fichiers, la mémoire, les liens, les pièces jointes et le trafic réseau. Ils ne sont pas équipés pour comprendre et analyser les interactions spécifiques au sein du navigateur, qui devient le véritable environnement d'exécution.

#### Recherche "Own the Browser" :

Une étude indépendante a examiné la sécurité et la gouvernance de plus de 20 navigateurs. Elle a révélé une abondance de politiques, mais un manque de visibilité sur la manière dont elles s'appliquent au comportement réel des utilisateurs.

#### L'impact de l'IA :

Les outils d'IA et les navigateurs dédiés à l'IA exacerbent ce problème en normalisant et en facilitant le mouvement de données sensibles via le navigateur. L'activité, bien que potentiellement risquée, semble souvent légitime, rendant l'évaluation du risque sans contexte complexe.

#### Bénéfices d'une observabilité au niveau du navigateur :

Une visibilité accrue des activités du navigateur permet :

*   **Prévention plus efficace :** Définir des contrôles plus précis et ciblés pour prévenir les actions risquées au moment où elles se produisent.
*   **Amélioration de la détection :** Évaluer le comportement dans son contexte.
*   **Réponse facilitée :** Reconstituer les incidents pour une meilleure compréhension.
*   **Affinement des politiques :** Adapter les règles de sécurité en fonction de l'usage réel.

Sans cette visibilité, les entreprises peuvent se retrouver dans l'incapacité de prévenir et d'expliquer ces attaques.

---
[Source](https://www.bleepingcomputer.com/news/security/edr-email-and-sase-miss-this-entire-class-of-browser-attacks/){:target="_blank"}
