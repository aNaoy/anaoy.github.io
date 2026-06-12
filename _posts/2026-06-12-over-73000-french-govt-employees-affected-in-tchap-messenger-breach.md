---
title: 'Over 73,000 French govt employees affected in Tchap messenger breach'
date: 2026-06-12
permalink: /posts/2026/06/12/over-73000-french-govt-employees-affected-in-tchap-messenger-breach/
tags:
- veille-cyber
- bleepingcomp
---
### Violation de données sur la plateforme Tchap : 73 000 agents publics impactés

La DINUM a confirmé une intrusion sur Tchap, la messagerie chiffrée utilisée par l'administration française, affectant plus de 73 000 agents publics (environ 9 % des utilisateurs). L'attaquant a exploité un compte utilisateur compromis, potentiellement via une attaque par ingénierie sociale, pour accéder aux données exposées dans des salons de discussion publics non chiffrés.

**Points clés :**
* **Données compromises :** Noms, prénoms, adresses e-mail, avatars, informations sur l'organisation d'appartenance, ainsi que 13,5 Go de documents et fichiers partagés dans des salons publics.
* **Accès malveillant :** L'assaillant a pu extraire près de 650 000 messages et des identifiants LDAP codés en dur dans un script PowerShell.
* **État du service :** Les conversations privées chiffrées restent sécurisées. Le compte à l'origine de l'intrusion a été identifié et bloqué.
* **Vulnérabilités :**
    * **Ingénierie sociale :** Vecteur d'entrée initial pour la compromission d'un compte.
    * **Exposition de secrets :** Identifiants LDAP codés en dur (hardcoded credentials).
    * **Configuration des salons :** Absence de chiffrement sur les canaux de communication publics, facilitant le vol de données en masse.

**Recommandations :**
* **Renforcement de l'authentification :** Implémenter et exiger systématiquement l'authentification multifacteur (MFA) pour tous les comptes afin de limiter l'impact des identifiants compromis.
* **Gestion des secrets :** Supprimer les identifiants codés en dur dans les scripts ; privilégier l'utilisation de coffres-forts numériques (vaults) ou de gestionnaires de secrets.
* **Sensibilisation :** Renforcer la formation des agents publics aux techniques d'ingénierie sociale (phishing, usurpation d'identité).
* **Audit de configuration :** Réviser les paramètres de visibilité des espaces de discussion et appliquer des politiques strictes de partage de fichiers sensibles.

---
[Source](https://www.bleepingcomputer.com/news/security/french-govt-says-tchap-breach-affected-over-73-000-accounts/){:target="_blank"}
