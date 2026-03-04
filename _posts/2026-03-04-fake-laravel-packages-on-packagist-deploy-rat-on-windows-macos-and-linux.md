---
title: 'Fake Laravel Packages on Packagist Deploy RAT on Windows, macOS, and Linux'
date: 2026-03-04
permalink: /posts/2026/03/04/fake-laravel-packages-on-packagist-deploy-rat-on-windows-macos-and-linux/
tags:
- veille-cyber
- hackernews
---
### Chevaux de Troie d'Accès à Distance dans des Packages Laravel Malveillants

Des chercheurs en cybersécurité ont identifié plusieurs packages PHP pour Laravel, disponibles sur Packagist, qui dissimulent un cheval de Troie d'accès à distance (RAT). Ces packages, nommés "nhattuanbl/lara-helper", "nhattuanbl/simple-queue", et "nhattuanbl/lara-swagger", sont capables d'infecter les systèmes Windows, macOS et Linux.

Le package "nhattuanbl/lara-swagger", bien que n'intégrant pas directement de code malveillant, déclare "nhattuanbl/lara-helper" comme dépendance Composer. Lors de l'installation, "nhattuanbl/lara-helper" déploie le RAT. Les packages infectés contiennent un fichier PHP obfusqué ("src/helper.php") conçu pour échapper à l'analyse statique.

Une fois activé, le RAT établit une connexion avec un serveur de commande et de contrôle (C2) à l'adresse helper.leuleu[.]net:2096. Il transmet des informations sur le système de la victime et attend des commandes, accordant ainsi à l'attaquant un accès complet à distance.

**Points Clés :**

*   **Nature de la Menace :** Packages PHP malveillants déguisés en utilitaires Laravel, déployant un RAT multiplateforme.
*   **Mécanisme d'Infection :** Via les dépendances Composer, notamment lorsque "nhattuanbl/lara-swagger" est utilisé, ce qui entraîne l'installation de "nhattuanbl/lara-helper".
*   **C2 Communication :** Utilisation de `stream_socket_client()` en TCP vers helper.leuleu[.]net:2096.
*   **Fonctionnalités du RAT :** Envoi de la reconnaissance système, exécution de commandes shell (popen, proc_open, exec, shell_exec, system, passthru), capture d'écran, téléchargement/téléversement de fichiers.
*   **Persistance :** Le RAT tente de se reconnecter au serveur C2 toutes les 15 secondes.
*   **Impact :** L'attaquant obtient un accès complet au shell, la capacité de lire/écrire des fichiers arbitraires, et d'accéder aux informations d'identification sensibles présentes dans l'environnement de l'application (clés API, fichiers .env).
*   **Stratégie de l'Attaquant :** Publication de packages légitimes ("nhattuanbl/lara-media", "nhattuanbl/snooze", "nhattuanbl/syslog") pour établir une fausse crédibilité.

**Vulnérabilités / Packages Malveillants :**

*   `nhattuanbl/lara-helper` (37 téléchargements)
*   `nhattuanbl/simple-queue` (29 téléchargements)
*   `nhattuanbl/lara-swagger` (49 téléchargements)

Aucun numéro CVE n'est spécifiquement associé à ces packages dans l'article, la vulnérabilité résidant dans le code malveillant qu'ils contiennent.

**Recommandations :**

*   Les utilisateurs ayant installé ces packages doivent considérer leur système comme compromis.
*   Supprimer immédiatement les packages suspects.
*   Rotation de tous les secrets accessibles depuis l'environnement de l'application (clés API, identifiants de base de données).
*   Auditer le trafic sortant pour identifier les communications vers le serveur C2.
*   Vérifier la présence de codes obfusqués dans les dépendances.

---
[Source](https://thehackernews.com/2026/03/fake-laravel-packages-on-packagist.html){:target="_blank"}
