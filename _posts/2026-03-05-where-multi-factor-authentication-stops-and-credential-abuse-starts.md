---
title: 'Where Multi-Factor Authentication Stops and Credential Abuse Starts'
date: 2026-03-05
permalink: /posts/2026/03/05/where-multi-factor-authentication-stops-and-credential-abuse-starts/
tags:
- veille-cyber
- hackernews
---
### Au-delà de l'authentification multifacteur : sécuriser les accès Windows

Si l'authentification multifacteur (MFA) est efficace pour les applications cloud et les identités fédérées, elle reste insuffisante dans les environnements Windows où les accès s'appuient souvent sur des processus Active Directory (AD) natifs non protégés par des jetons MFA.

**Points clés et vecteurs d'attaque :**
Les attaquants exploitent sept chemins d'authentification principaux pour contourner les contrôles modernes :
1. **Logon interactif Windows :** Les connexions directes aux postes de travail ou serveurs (via Kerberos/NTLM) ignorent les politiques MFA des fournisseurs d'identité cloud.
2. **Accès RDP :** Les sessions bureau à distance permettent des mouvements latéraux sans déclencher de contrôle MFA.
3. **Protocole NTLM :** Vulnérable aux attaques de type *pass-the-hash*, il permet de s'authentifier avec un simple hash plutôt qu'un mot de passe en clair.
4. **Abus de tickets Kerberos :** Le vol ou la falsification de tickets (Golden/Silver Tickets) offre aux attaquants un accès persistant et discret.
5. **Comptes administrateur locaux :** La réutilisation de mots de passe d'administration locale facilite l'escalade de privilèges sur tout le parc informatique.
6. **SMB (Server Message Block) :** Utilisé pour le mouvement latéral, il traite souvent les connexions comme du trafic interne sécurisé.
7. **Comptes de service :** Disposant de droits étendus et de mots de passe statiques, ils constituent des cibles privilégiées car ils ne supportent généralement pas le MFA.

**Recommandations de sécurité :**
* **Renforcer les politiques de mots de passe AD :** Imposer des phrases de passe longues (15+ caractères) et interdire les schémas faibles.
* **Bloquer les mots de passe compromis :** Utiliser des solutions vérifiant en continu les mots de passe utilisés contre des bases de données de fuites de données connues (plus de 5,4 milliards d'identifiants).
* **Réduire l'usage des protocoles hérités :** Identifier et restreindre l'utilisation de NTLM au profit de Kerberos.
* **Gestion stricte des comptes de service :** Inventorier, limiter les privilèges (principe du moindre privilège) et effectuer une rotation régulière des identifiants.
* **Étendre le MFA :** Implémenter des solutions capables d'appliquer le MFA aux sessions locales, VPN et RDP, comblant ainsi les lacunes de l'Active Directory.

---
[Source](https://thehackernews.com/2026/03/where-multi-factor-authentication-stops.html){:target="_blank"}
