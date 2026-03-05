---
title: 'Where Multi-Factor Authentication Stops and Credential Abuse Starts'
date: 2026-03-05
permalink: /posts/2026/03/05/where-multi-factor-authentication-stops-and-credential-abuse-starts/
tags:
- veille-cyber
- hackernews
---
**L'Authentification Multi-Facteurs et les Limites de la Protection des Identifiants Windows**

Malgré la mise en place de l'authentification multi-facteurs (MFA), les environnements Windows restent vulnérables aux attaques basées sur des identifiants volés. La couverture de la MFA est souvent incomplète, car de nombreuses méthodes d'authentification Windows, notamment celles liées à Active Directory (AD) local, ne déclenchent pas systématiquement les mécanismes de MFA conçus pour les applications cloud et les connexions fédérées. Les attaquants exploitent ces lacunes pour compromettre les réseaux.

**Points Clés :**

*   **Lacunes de la MFA :** La MFA est efficace pour les applications cloud et les connexions fédérées via un fournisseur d'identité (IdP) comme Entra ID, Okta, ou Google Workspace. Cependant, elle ne protège pas toujours les authentifications locales ou directes sur les systèmes Windows joints à un domaine.
*   **Vulnérabilités d'Authentification Windows :** Sept chemins d'authentification sont particulièrement ciblés par les attaquants :
    1.  **Connexion interactive Windows :** Les connexions directes à une station de travail ou un serveur Windows sont généralement gérées par AD et peuvent contourner la MFA si des mécanismes comme Windows Hello for Business ou les cartes à puce ne sont pas implémentés.
    2.  **Accès RDP direct :** Les connexions RDP, même internes, peuvent ne pas passer par les contrôles MFA basés sur le cloud, reposant uniquement sur les identifiants AD.
    3.  **Authentification NTLM :** Ce protocole hérité, bien que déprécié, est toujours utilisé et vulnérable aux techniques comme le "pass-the-hash", qui ne nécessitent pas le mot de passe en clair et ne sont pas bloquées par la MFA.
    4.  **Abus de tickets Kerberos :** Le vol ou la falsification de tickets Kerberos permet aux attaquants de maintenir un accès, de se déplacer latéralement et d'éviter la détection.
    5.  **Comptes administrateurs locaux et réutilisation d'identifiants :** La réutilisation de mots de passe pour les comptes administrateurs locaux permet une escalade de privilèges rapide et contourne la MFA d'Entra ID.
    6.  **Authentification SMB et mouvement latéral :** L'utilisation du protocole SMB pour le partage de fichiers et l'accès aux ressources permet aux attaquants de se déplacer entre les systèmes une fois qu'ils ont des identifiants valides, sans que la MFA soit toujours appliquée.
    7.  **Comptes de service sans MFA :** Les comptes de service, utilisés pour les tâches automatisées, ont souvent des identifiants stables, des permissions étendues et ne sont pas protégés par la MFA en raison de leur nature automatisée.

**Recommandations :**

*   **Politiques de mots de passe renforcées dans AD :** Implémenter des politiques exigeant des phrases de passe plus longues (15 caractères minimum), interdisant la réutilisation et les schémas faibles.
*   **Blocage continu des mots de passe compromis :** Utiliser des bases de données de mots de passe divulgués pour empêcher les utilisateurs de définir des identifiants déjà compromis.
*   **Réduction de l'exposition aux protocoles d'authentification hérités :** Restreindre ou éliminer l'utilisation de NTLM autant que possible et renforcer les contrôles là où il ne peut être supprimé.
*   **Audit des comptes de service et réduction des privilèges excessifs :** Examiner, limiter les permissions inutiles, faire pivoter les identifiants et supprimer les comptes de service non utilisés. Traiter les comptes de service avec des permissions de domaine comme des cibles à haut risque.
*   **Implémenter la MFA pour les connexions Windows locales et RDP :** Utiliser des solutions qui étendent la protection MFA aux points d'accès Windows, y compris les connexions hors ligne et RDP.

---
[Source](https://thehackernews.com/2026/03/where-multi-factor-authentication-stops.html){:target="_blank"}
