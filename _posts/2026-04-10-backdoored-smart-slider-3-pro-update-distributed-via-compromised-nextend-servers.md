---
title: 'Backdoored Smart Slider 3 Pro Update Distributed via Compromised Nextend Servers'
date: 2026-04-10
permalink: /posts/2026/04/10/backdoored-smart-slider-3-pro-update-distributed-via-compromised-nextend-servers/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne d'approvisionnement : Backdoor dans Smart Slider 3 Pro

Une attaque par compromission de la chaîne d'approvisionnement a ciblé les serveurs de mise à jour de Nextend, permettant l'injection d'une version malveillante (3.5.1.35) du plugin **Smart Slider 3 Pro** pour WordPress. Cette version, distribuée pendant environ six heures, contenait un toolkit d'accès distant sophistiqué.

**Points clés :**
* **Type d'attaque :** Compromission de la chaîne d'approvisionnement (Supply Chain Attack).
* **Vecteur :** Serveur de mise à jour officiel de Nextend.
* **Impact :** Exécution de code à distance (RCE) pré-authentifiée, création de comptes administrateurs cachés et exfiltration de données sensibles vers le domaine `wpjs1[.]com`.
* **Vulnérabilités :** L'attaque exploite une porte dérobée permettant l'exécution de commandes système via des en-têtes HTTP personnalisés (`X-Cache-Key`) et l'exécution de code PHP arbitraire via des paramètres cachés. (Aucun identifiant CVE spécifique n'a été attribué à ce stade, l'incident étant le résultat direct d'une intrusion système).

**Fonctionnalités du malware :**
* **Persistance redondante :** Utilisation de fichiers "must-use" (`object-cache-helper.php`), modification de `functions.php` et ajout de scripts dans `wp-includes`.
* **Dissimulation :** Masquage des comptes administrateurs créés via une manipulation des filtres de requêtes utilisateur et stockage des données dans des options WordPress non indexées (`_wpc_ak`, `_wpc_uid`, `_wpc_uinfo`).

**Recommandations :**
1. **Mise à jour immédiate :** Passer à la version **3.5.1.36** ou supérieure.
2. **Nettoyage complet :** 
   * Supprimer les comptes administrateurs suspects.
   * Supprimer les fichiers de persistance identifiés (`object-cache-helper.php`, `class-wp-locale-helper.php`).
   * Nettoyer la table `wp_options` (supprimer les clés `_wpc_...`).
   * Restaurer les fichiers `wp-config.php` et `.htaccess` d'origine.
3. **Réinitialisation des accès :** Modifier tous les mots de passe (administrateurs, base de données, FTP/SSH).
4. **Sécurisation renforcée :** Activer l'authentification à deux facteurs (2FA) et désactiver l'exécution PHP dans les répertoires d'upload.

---
[Source](https://thehackernews.com/2026/04/backdoored-smart-slider-3-pro-update.html){:target="_blank"}
