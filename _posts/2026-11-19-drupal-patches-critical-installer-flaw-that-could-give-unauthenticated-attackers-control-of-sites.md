---
title: 'Drupal Patches Critical Installer Flaw That Could Give Unauthenticated Attackers Control of Sites'
date: 2026-11-19
permalink: /posts/2026/11/19/drupal-patches-critical-installer-flaw-that-could-give-unauthenticated-attackers-control-of-sites/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans l'installeur Drupal : Risque de prise de contrôle totale

Une vulnérabilité critique a été identifiée dans le cœur de Drupal, permettant à un attaquant non authentifié d'accéder au fichier `install.php` pour réinstaller un site, ce qui peut conduire à une exécution de code à distance (RCE) et à une prise de contrôle complète du serveur.

**Points clés :**
*   **Vulnérabilité :** CVE-2026-132165.
*   **Risque :** Classée critique, avec une preuve de concept existante.
*   **Complexité :** L'exploitation est jugée complexe et dépend des configurations spécifiques du serveur (notamment si le fichier `settings.php` est accessible en écriture).
*   **Origine :** Découverte par le service "OSS Scanner" d'Anthropic.
*   **Contexte :** Drupal fait face à une augmentation des signalements de vulnérabilités via des outils d'IA, entraînant une réduction future du support des versions mineures.

**Versions affectées :**
*   Toutes les versions inférieures à 10.6.22.
*   Drupal 11.0.x à 11.3.x (avant 11.3.22).
*   Drupal 11.4.0 (avant 11.4.13).
*   *Note : Les versions 8, 9, 10.5.x et inférieures sont en fin de vie (EOL) et ne recevront pas de correctif.*

**Recommandations :**
1.  **Mise à jour immédiate :** Passer aux versions 10.6.22, 11.3.22 ou 11.4.13 selon la branche utilisée.
2.  **Sécurisation supplémentaire :** Même après mise à jour, il est vivement conseillé de bloquer l'accès au fichier `/core/install.php` via des règles dans le serveur web (Nginx/Apache) ou des fichiers `.htaccess`.
3.  **Suppression :** Si l'installation est terminée, supprimer physiquement le fichier `install.php` et s'assurer qu'il ne soit pas restauré par les outils de déploiement (Composer).

---
[Source](https://thehackernews.com/2026/11/drupal-patches-critical-installer-flaw.html){:target="_blank"}
