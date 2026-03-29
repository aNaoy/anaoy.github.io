---
title: 'File read flaw in Smart Slider plugin impacts 500K WordPress sites'
date: 2026-03-29
permalink: /posts/2026/03/29/file-read-flaw-in-smart-slider-plugin-impacts-500k-wordpress-sites/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique de lecture de fichiers dans Smart Slider 3

Une faille de sécurité majeure affecte le plugin WordPress « Smart Slider 3 », utilisé par plus de 800 000 sites. Elle permet à un utilisateur authentifié (même avec un compte simple de type « abonné ») d'exfiltrer des fichiers sensibles situés sur le serveur.

**Points clés :**
*   **Impact :** Environ 500 000 sites utilisent toujours une version vulnérable du plugin.
*   **Risque :** Un attaquant peut accéder au fichier `wp-config.php`, compromettant ainsi les identifiants de base de données, les clés de chiffrement et permettant potentiellement une prise de contrôle totale du site.
*   **Cause :** L'absence de vérification des capacités et de validation des types de fichiers dans la fonction d'exportation AJAX du plugin. La présence d'un *nonce* ne suffit pas à bloquer l'exploitation car il peut être facilement récupéré par un utilisateur connecté.

**Vulnérabilité identifiée :**
*   **CVE-2026-3098 :** Faille de lecture arbitraire de fichiers, présente dans toutes les versions de Smart Slider 3 jusqu'à la 3.5.1.33.

**Recommandations :**
*   **Mise à jour immédiate :** Les administrateurs doivent mettre à jour le plugin vers la version **3.5.1.34** ou supérieure, publiée par Nextendweb pour corriger cette faille.
*   **Surveillance :** Bien qu'aucune exploitation active ne soit signalée, la nature critique de la faille impose une action rapide pour sécuriser les sites possédant des options d'inscription ou d'abonnement.

---
[Source](https://www.bleepingcomputer.com/news/security/file-read-flaw-in-smart-slider-plugin-impacts-500k-wordpress-sites/){:target="_blank"}
