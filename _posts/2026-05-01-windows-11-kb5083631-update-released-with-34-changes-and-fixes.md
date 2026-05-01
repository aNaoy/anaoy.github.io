---
title: 'Windows 11 KB5083631 update released with 34 changes and fixes'
date: 2026-05-01
permalink: /posts/2026/05/01/windows-11-kb5083631-update-released-with-34-changes-and-fixes/
tags:
- veille-cyber
- bleepingcomp
---
### Mise à jour Windows 11 KB5083631 : Améliorations fonctionnelles et sécurité

Microsoft a publié la mise à jour cumulative optionnelle **KB5083631** pour Windows 11, introduisant 34 changements destinés à améliorer la performance et la sécurité. Étant une version de prévisualisation, cette mise à jour ne contient pas de correctifs de sécurité critiques, mais prépare le terrain pour les déploiements du prochain « Patch Tuesday ».

**Points clés :**
*   **Nouvelles fonctionnalités :** Introduction d'un mode "Xbox" (interface plein écran dédiée aux jeux) et support du retour haptique pour certains périphériques d'entrée.
*   **Optimisation :** Amélioration du temps de lancement des applications au démarrage et corrections de bugs sur l'Explorateur de fichiers.
*   **Batch et Scripting :** Mise en place d'un mode de traitement sécurisé empêchant la modification des fichiers batch (.bat) durant leur exécution.
*   **Secure Boot :** Déploiement progressif de nouveaux certificats Secure Boot pour remplacer ceux de 2011 expirant en juin 2026.
*   **Authentification :** Correction d'une erreur d'authentification Kerberos (0xc000009a) lors de sessions via Remote Credential Guard.

**Vulnérabilités traitées :**
*   **CVE-2024-30098 :** Cette mise à jour améliore la journalisation des événements liée à cette vulnérabilité. L'ajout du nom de l'application affectée facilite désormais l'identification des logiciels dépendant de certificats de carte à puce nécessitant une mise à jour suite aux récents changements de sécurité.

**Recommandations :**
*   **Installation :** Cette mise à jour étant optionnelle, elle doit être téléchargée manuellement via *Paramètres > Windows Update* en cliquant sur « Télécharger et installer ».
*   **Attention BitLocker :** Les administrateurs de serveurs sous Windows Server 2025 utilisant des configurations BitLocker spécifiques doivent être vigilants : une saisie de la clé de récupération peut être requise lors du premier redémarrage après l'installation.
*   **Maintenance des certificats :** Il est conseillé de surveiller le déploiement des nouveaux certificats Secure Boot pour éviter tout problème de démarrage à l'approche de la date d'expiration en juin 2026.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/windows-11-kb5083631-update-released-with-34-changes-and-fixes/){:target="_blank"}
