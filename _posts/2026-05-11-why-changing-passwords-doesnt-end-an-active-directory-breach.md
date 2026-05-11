---
title: 'Why Changing Passwords Doesn’t End an Active Directory Breach'
date: 2026-05-11
permalink: /posts/2026/05/11/why-changing-passwords-doesnt-end-an-active-directory-breach/
tags:
- veille-cyber
- bleepingcomp
---
### Pourquoi réinitialiser les mots de passe ne suffit pas en cas de compromission Active Directory

La réinitialisation des mots de passe est une réponse réflexe courante en cas de piratage, mais elle s'avère souvent insuffisante pour expulser un attaquant de manière définitive. Dans les environnements Active Directory (AD) et hybrides (Entra ID), une réinitialisation ne garantit pas une invalidation immédiate des accès sur tous les points d'authentification.

#### Points clés
*   **La persistance par le cache :** Les systèmes Windows conservent des hashs de mots de passe en cache local. Tant qu'une machine ne se reconnecte pas au domaine, l'ancien hash peut rester fonctionnel.
*   **Les sessions actives et tickets Kerberos :** Une fois qu'un attaquant possède un ticket d'authentification valide, il peut continuer à accéder aux ressources sans avoir besoin du nouveau mot de passe jusqu'à l'expiration du ticket.
*   **La synchronisation hybride :** Un délai existe entre le changement du mot de passe dans AD et sa synchronisation vers le cloud (Entra ID), offrant une fenêtre d'opportunité aux attaquants.
*   **La persistance par les privilèges :** Si l'attaquant a modifié des ACL (listes de contrôle d'accès) ou ajouté des comptes de service, il peut conserver un accès permanent malgré le changement de mot de passe des comptes utilisateurs.

#### Vulnérabilités exploitées
*   **Pass-the-Hash :** Utilisation des hashs capturés avant la réinitialisation pour s'authentifier.
*   **Kerberoasting :** Extraction des mots de passe des comptes de service.
*   **Attaques sur les tickets Kerberos :** Utilisation de **Golden Tickets** (compromission du compte KRBTGT) ou de **Silver Tickets** pour contourner totalement la nécessité d'un mot de passe valide.
*   **Manipulation d'objets privilégiés :** Modification de l'objet **AdminSDHolder** pour réappliquer automatiquement des droits sur des comptes administrateurs via le processus SDProp.

#### Recommandations pour une éviction efficace
*   **Invalider les accès actifs :** Forcer la déconnexion des sessions et redémarrer les systèmes pour purger les tickets Kerberos en mémoire.
*   **Réinitialisation critique :** En cas de compromission grave, réinitialiser deux fois le compte **KRBTGT** pour invalider tous les tickets Kerberos émis par le contrôleur de domaine.
*   **Gestion des comptes de service :** Procéder à une rotation systématique des mots de passe des comptes de service, particulièrement ceux disposant de privilèges élevés.
*   **Audit approfondi :** Vérifier les modifications récentes sur les appartenances aux groupes, les droits délégués et les ACL (notamment sur les objets sensibles comme AdminSDHolder).
*   **Sécurisation du processus de reset :** Mettre en place des solutions permettant une mise à jour immédiate du cache local sur les endpoints lors de la réinitialisation pour réduire la surface d'attaque.

---
[Source](https://www.bleepingcomputer.com/news/security/why-changing-passwords-doesnt-end-an-active-directory-breach/){:target="_blank"}
