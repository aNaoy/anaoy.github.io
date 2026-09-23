---
title: 'A Leaked GitLab Issue Email Address Lets Anyone Push Code and Run CI Jobs as You'
date: 2026-09-23
permalink: /posts/2026/09/23/a-leaked-gitlab-issue-email-address-lets-anyone-push-code-and-run-ci-jobs-as-you/
tags:
- veille-cyber
- hackernews
---
### Risque critique lié aux adresses e-mail de projet GitLab

Une vulnérabilité de conception dans GitLab permet à quiconque possédant l'adresse e-mail dédiée à la création d'issues de se faire passer pour le propriétaire du compte. En utilisant cette adresse, un attaquant peut soumettre des correctifs, modifier des branches (y compris `main`) et exécuter des jobs CI/CD avec les privilèges de la victime, sans aucune vérification d'identité ou authentification à deux facteurs (2FA).

**Points clés :**
*   **Token statique :** L'adresse e-mail contient un jeton unique par utilisateur qui ne possède pas de date d'expiration.
*   **Contournement des protections :** La réception d'e-mails ignore les restrictions IP et la 2FA, même sur les instances où ces mesures sont obligatoires.
*   **Portée de l'attaque :** Un attaquant peut transformer une demande d'issue en "merge request" en modifiant simplement le suffixe de l'adresse e-mail. Le niveau d'accès dépend des permissions réelles de l'utilisateur compromis (ex: un utilisateur avec des droits "Maintainer" expose les secrets CI/CD).
*   **Vulnérabilité de conception :** GitLab considère ce comportement comme "conforme aux spécifications" (intended behavior), traitant le jeton comme une simple information d'identification.

**Vulnérabilités :**
*   Aucun identifiant CVE n'a été attribué, GitLab classant ce comportement comme une fonctionnalité par défaut et non comme un bug.

**Recommandations :**
*   **Réinitialisation immédiate :** Changez votre jeton d'e-mail entrant via la page des jetons d'accès personnels de votre profil. Cela invalidera immédiatement toutes les anciennes adresses e-mail générées.
*   **Audit public :** Vérifiez vos fichiers `README`, guides de contribution et pages de support pour vous assurer qu'aucune adresse e-mail personnelle liée à ce service n'a été publiée accidentellement.
*   **Configuration instance :** Pour les instances auto-hébergées, les administrateurs peuvent désactiver la fonctionnalité d'e-mails entrants au niveau global pour réduire la surface d'attaque.
*   **Prudence :** Ne partagez jamais ces adresses e-mail de projet, car elles agissent comme des identifiants d'authentification permanente.

---
[Source](https://thehackernews.com/2026/09/a-leaked-gitlab-issue-email-address.html){:target="_blank"}
