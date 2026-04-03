---
title: 'Man admits to locking thousands of Windows devices in extortion plot'
date: 2026-04-03
permalink: /posts/2026/04/03/man-admits-to-locking-thousands-of-windows-devices-in-extortion-plot/
tags:
- veille-cyber
- bleepingcomp
---
### Sabotage et tentative d'extorsion par un ex-ingénieur infrastructure

Daniel Rhyne, ancien ingénieur infrastructure, a plaidé coupable d'avoir orchestré une cyberattaque contre son employeur pour obtenir une rançon de 20 bitcoins (environ 750 000 $). En utilisant des accès administrateur légitimes, il a verrouillé des centaines de serveurs et postes de travail avant d'être appréhendé.

**Points clés :**
* **Nature de l'attaque :** Utilisation de comptes à privilèges pour modifier les mots de passe de 13 comptes administrateurs de domaine, 301 comptes utilisateurs et des accès locaux sur 3 284 postes et 254 serveurs.
* **Mode opératoire :** Automatisation via des tâches planifiées sur le contrôleur de domaine pour supprimer des comptes administrateurs, modifier des mots de passe et programmer des arrêts systèmes aléatoires.
* **Intention :** Extorsion par rançon, incluant la menace de destruction de sauvegardes pour rendre la récupération impossible.
* **Détection :** Les administrateurs réseau ont été alertés par une vague massive de notifications de réinitialisation de mots de passe, révélant la suppression des comptes administrateurs de domaine.

**Vulnérabilités exploitées :**
* Aucune CVE spécifique n'est associée, car il s'agit d'un cas d'**abus de privilèges (Insider Threat)**. L'attaque repose sur l'exploitation des droits d'administration légitimes pour exécuter des commandes système (Net user, suppression de comptes AD).

**Recommandations de sécurité :**
* **Moindre privilège :** Appliquer strictement le principe du moindre privilège, même pour les ingénieurs infrastructure, en limitant les droits d'administration globale aux seules opérations nécessaires.
* **Gestion des accès (PAM) :** Mettre en œuvre des solutions de gestion des accès à privilèges (Privileged Access Management) pour surveiller, enregistrer et restreindre les commandes sensibles.
* **Immuabilité des sauvegardes :** Garantir que les sauvegardes sont isolées, immuables et déconnectées du réseau principal pour éviter toute suppression malveillante.
* **Surveillance du comportement :** Mettre en place une journalisation robuste (SIEM) capable d'alerter sur des modifications massives et suspectes de comptes (ex: suppression simultanée de plusieurs comptes admin).
* **Séparation des tâches :** Éviter qu'un seul administrateur puisse modifier l'intégralité de l'infrastructure sans supervision ou approbation multi-utilisateurs.

---
[Source](https://www.bleepingcomputer.com/news/security/man-admits-to-extortion-plot-locking-coworkers-out-of-thousands-of-windows-devices/){:target="_blank"}
