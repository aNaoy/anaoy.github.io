---
title: 'Compromised Site Management Panels are a Hot Item in Cybercrime Markets'
date: 2026-03-03
permalink: /posts/2026/03/03/compromised-site-management-panels-are-a-hot-item-in-cybercrime-markets/
tags:
- veille-cyber
- bleepingcomp
---
### Marché noir des accès aux panneaux de gestion de sites web

Des acteurs malveillants vendent activement des accès à des panneaux de gestion de sites web compromis, le plus souvent des comptes cPanel, sur des forums clandestins. Ces accès sont considérés comme des infrastructures "plug-and-play" pour des campagnes de phishing et d'escroquerie. L'analyse de milliers d'annonces montre un marché structuré où la qualité des comptes cPanel vendus varie selon des critères tels que la réputation du domaine (ex: .gov vs .xyz), la présence d'un serveur SMTP actif pour l'envoi d'emails, et la localisation géographique du serveur d'hébergement.

**Points clés :**

*   Les comptes cPanel compromis sont une marchandise populaire dans le cybercrime.
*   Ils servent de plateforme pour des activités malveillantes comme le phishing, l'envoi de spam, l'hébergement d'infrastructures frauduleuses et le vol de données.
*   Le marché est fortement "commoditisé" avec des annonces répétitives et des ventes en gros.
*   La confiance accordée aux domaines (ex: .gov, .mil) influence le prix.
*   L'accès à un serveur SMTP actif augmente la valeur d'un compte compromis.

**Vulnérabilités et Vecteurs d'attaque :**

Bien que l'article ne détaille pas de CVE spécifiques, il mentionne plusieurs méthodes courantes utilisées pour compromettre les comptes cPanel :

*   **Identifiants volés ou devinés :** Utilisation de campagnes de phishing, réutilisation de mots de passe issus de fuites de données, attaques par force brute contre les portails de connexion cPanel.
*   **Mauvaises configurations :** Exposition de fichiers sensibles (config.yaml, .env), mots de passe faibles, absence d'authentification multifacteur (MFA).
*   **Exploitation de sites web vulnérables hébergés sur le même serveur :** Plateformes CMS obsolètes (WordPress, Joomla, Drupal) et leurs plugins/thèmes vulnérables permettant l'injection de web shells ou l'escalade de privilèges.
*   **Automatisation :** Des botnets scannent en continu les panneaux de connexion exposés, les CVE connues et les mauvaises configurations.

**Recommandations :**

*   **Activer l'authentification multifacteur (MFA)** sur tous les comptes des panneaux de contrôle d'hébergement.
*   **Appliquer des mots de passe forts et uniques.**
*   **Restreindre l'accès administratif par adresse IP** lorsque cela est possible.
*   **Surveiller continuellement l'activité SMTP sortante** pour détecter les abus de spam.
*   Mettre en place une **surveillance de l'intégrité des fichiers** pour identifier les modifications non autorisées.
*   Suivre la création de nouveaux comptes d'hébergement, les tâches cron inattendues et les changements de configuration.
*   **Surveiller l'exposition des identifiants** dans les logs de "stealer" et sur les marchés clandestins.
*   **Maintenir à jour les plateformes CMS et leurs plugins.**
*   Désactiver les services inutiles et appliquer le **principe du moindre privilège**.

---
[Source](https://www.bleepingcomputer.com/news/security/compromised-site-management-panels-are-a-hot-item-in-cybercrime-markets/){:target="_blank"}
