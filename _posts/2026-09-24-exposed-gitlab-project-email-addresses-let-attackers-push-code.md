---
title: 'Exposed GitLab project email addresses let attackers push code'
date: 2026-09-24
permalink: /posts/2026/09/24/exposed-gitlab-project-email-addresses-let-attackers-push-code/
tags:
- veille-cyber
- bleepingcomp
---
### Risque d'usurpation via les adresses email GitLab

La fonctionnalité GitLab « Email work item to this project » permet aux développeurs de créer des tickets ou des demandes de fusion (*merge requests*) par courriel. Ces adresses contiennent un jeton d'authentification unique lié au compte de l'utilisateur. L'exposition publique de ces adresses (dans des fichiers README ou des guides de contribution) permet à un attaquant d'agir au nom du propriétaire du compte.

**Points clés :**
* **Fonctionnement :** Chaque adresse email contient un jeton (`glimt-`) qui authentifie les requêtes. GitLab traite les emails reçus comme provenant du détenteur du jeton.
* **Exploitation :** Un attaquant peut modifier le suffixe de l'adresse de `-issue` à `-merge-request` pour soumettre du code malveillant, accéder à des secrets CI/CD ou consulter des données confidentielles.
* **Contournement :** Cette méthode permet de contourner les restrictions d'adresse IP configurées sur le projet.
* **Statut :** GitLab considère ce comportement comme une fonctionnalité prévue et non comme une vulnérabilité logicielle classique (pas de CVE attribuée).

**Vulnérabilités :**
* Pas de CVE associée. Le problème réside dans l'exposition volontaire d'identifiants (jetons) par les utilisateurs et l'absence de vérification que l'expéditeur de l'email correspond au propriétaire du jeton.

**Recommandations :**
* **Retrait immédiat :** Supprimer toute mention d'adresses email de ce type dans la documentation publique, les fichiers README et les guides de contribution.
* **Réinitialisation des jetons :** Si une adresse a été exposée, le propriétaire du compte doit impérativement réinitialiser son jeton de messagerie dans les paramètres GitLab.
* **Prudence :** Ne jamais partager ces adresses privées, car elles agissent comme des mots de passe permettant d'interagir avec les dépôts au nom de l'utilisateur.

---
[Source](https://www.bleepingcomputer.com/news/security/exposed-gitlab-project-email-addresses-let-attackers-push-code/){:target="_blank"}
