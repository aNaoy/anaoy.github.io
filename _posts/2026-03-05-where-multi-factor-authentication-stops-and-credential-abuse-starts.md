---
title: 'Where Multi-Factor Authentication Stops and Credential Abuse Starts'
date: 2026-03-05
permalink: /posts/2026/03/05/where-multi-factor-authentication-stops-and-credential-abuse-starts/
tags:
- veille-cyber
- hackernews
---
### Les limites de l'authentification multifacteur (MFA) face au vol d'identifiants

L'implémentation de l'authentification multifacteur (MFA) est souvent considérée comme une protection suffisante contre l'utilisation de mots de passe volés. Cependant, dans les environnements Windows, cette hypothèse est rarement vraie. Les attaquants continuent de compromettre les réseaux en exploitant des identifiants valides, car la couverture de l'authentification multifacteur n'est pas toujours complète. L'MFA, lorsqu'il est géré par un fournisseur d'identité (IdP) comme Microsoft Entra ID, Okta ou Google Workspace, protège efficacement les applications cloud et les connexions fédérées. Néanmoins, de nombreuses connexions Windows s'appuient sur des chemins d'authentification Active Directory (AD) qui n'activent pas les invites MFA. Pour réduire les compromissions basées sur les identifiants, les équipes de sécurité doivent comprendre les points d'entrée de l'authentification Windows qui échappent aux contrôles de l'IdP.

**Points clés :**

*   L'MFA est généralement efficace pour les applications cloud et les connexions fédérées, mais pas toujours pour les connexions directes aux systèmes Windows.
*   De nombreuses méthodes d'authentification Windows ne déclenchent pas l'MFA, laissant des vulnérabilités exploitables.
*   Les attaquants ciblent spécifiquement ces chemins d'authentification non couverts par l'MFA.

**Vulnérabilités et voies d'attaque exploitées :**

1.  **Connexion interactive Windows (locale ou jointe au domaine) :** L'authentification directe sur un poste de travail ou un serveur Windows utilise généralement AD (Kerberos ou NTLM) plutôt qu'un IdP cloud. Les mots de passe ou hashes NTLM volés permettent une connexion aux systèmes joints au domaine sans déclencher d'MFA.
2.  **Accès RDP direct :** Les sessions RDP directes ne passent pas systématiquement par les contrôles MFA basés sur le cloud, s'appuyant sur les identifiants AD sous-jacents.
3.  **Authentification NTLM :** Ce protocole hérité, bien que déprécié, est encore utilisé et supporte des techniques comme "pass-the-hash", où le hash NTLM suffit pour l'authentification, contournant l'MFA.
4.  **Abus de tickets Kerberos :** Les attaquants volent ou forgent des tickets Kerberos pour obtenir un accès persistant et se déplacer latéralement dans le réseau, indépendamment de la réinitialisation des mots de passe. Les techniques incluent "pass-the-ticket", "Golden Ticket" et "Silver Ticket".
5.  **Comptes administrateurs locaux et réutilisation d'identifiants :** La réutilisation des mots de passe des comptes administrateurs locaux sur plusieurs machines permet aux attaquants d'étendre rapidement une compromission. Ces comptes s'authentifient localement, ignorant les contrôles MFA.
6.  **Authentification SMB et mouvement latéral :** SMB, utilisé pour le partage de fichiers et l'accès à distance, est une voie fréquente pour le mouvement latéral. Si cette authentification est considérée comme interne, l'MFA y est rarement appliqué.
7.  **Comptes de service sans MFA :** Les comptes de service, utilisés pour les tâches automatisées et les applications, ont souvent des identifiants stables et des permissions étendues. Leur authentification étant automatisée, ils sont difficiles à protéger par MFA et sont une cible privilégiée.

**Recommandations :**

*   **Politiques de mots de passe renforcées dans AD :** Imposer des phrases de passe plus longues (plus de 15 caractères), empêcher la réutilisation des mots de passe et bloquer les modèles faibles.
*   **Blocage continu des mots de passe compromis :** Empêcher l'utilisation de mots de passe déjà exposés dans des fuites de données.
*   **Réduction de l'exposition aux protocoles d'authentification hérités :** Restreindre ou éliminer l'utilisation de NTLM lorsque cela est possible et renforcer les contrôles là où il ne peut être supprimé.
*   **Audit des comptes de service et réduction des privilèges excessifs :** Identifier, réduire les permissions inutiles, faire pivoter les identifiants et supprimer les comptes de service obsolètes. Traiter les comptes de service avec des permissions de domaine comme des cibles à haut risque.
*   **Implémenter l'MFA pour les connexions Windows :** Utiliser des solutions comme Windows Hello for Business, les cartes à puce, ou des outils tiers pour appliquer l'MFA aux connexions locales, RDP et VPN.

---
[Source](https://thehackernews.com/2026/03/where-multi-factor-authentication-stops.html){:target="_blank"}
