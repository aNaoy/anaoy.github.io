---
title: 'Windows 11 KB5101684 update released with 42 changes and fixes'
date: 2026-07-29
permalink: /posts/2026/07/29/windows-11-kb5101684-update-released-with-42-changes-and-fixes/
tags:
- veille-cyber
- bleepingcomp
---
### Mise à jour Windows 11 KB5101684 : Correctifs et nouvelles fonctionnalités

Microsoft a publié la mise à jour cumulative optionnelle **KB5101684** pour Windows 11 24H2 et 25H2, apportant 42 correctifs de bugs ainsi que diverses améliorations de fonctionnalités. Contrairement aux mises à jour du "Patch Tuesday", celle-ci est facultative et n'inclut pas de correctifs de sécurité critiques.

#### Points clés
* **Améliorations de l'interface :** Navigation optimisée dans l'Explorateur de fichiers, nouveaux indicateurs de taille de fichiers et contrôles de pavé tactile enrichis.
* **Productivité et Accessibilité :** Introduction de l'isolation vocale pour la reconnaissance vocale et support du coréen.
* **Sécurité :** Extension de la sécurité de connexion améliorée (*Enhanced Sign-in Security*) aux lecteurs d'empreintes digitales externes compatibles.
* **Fiabilité système :** Stabilité renforcée des applications Office en environnements virtualisés et meilleure gestion de l'alimentation.

#### Vulnérabilités traitées
L'article ne mentionne aucune CVE spécifique pour cette mise à jour, car il s'agit d'une version de prévisualisation non liée à la sécurité. Toutefois, elle corrige des comportements système problématiques :
* **Gestion des accès :** Résolution d'une erreur d'identification erronée lors de sauvegardes réseau (SMB).
* **Conformité MDM :** Correction d'un problème empêchant les appareils nouvellement enrôlés via MDM (Intune) d'accéder aux ressources d'entreprise.
* **Marquage de fichiers :** Correction d'une erreur de sécurité dans l'Explorateur où des fichiers locaux sur des lecteurs DFS étaient indûment marqués comme provenant d'Internet ("Mark of the Web").

#### Recommandations
* **Installation :** Puisqu'il s'agit d'une mise à jour optionnelle, elle peut être installée via **Paramètres > Windows Update > Vérifier les mises à jour**.
* **Déploiement :** Pour les environnements d'entreprise, il est recommandé de tester ces correctifs avant un déploiement massif, notamment pour valider les améliorations liées aux outils MDM et aux partages DFS.
* **Automatisation :** Si l'option "Obtenir les dernières mises à jour dès qu'elles sont disponibles" est activée, cette mise à jour pourra s'installer automatiquement.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/windows-11-kb5101684-update-released-with-42-changes-and-fixes/){:target="_blank"}
