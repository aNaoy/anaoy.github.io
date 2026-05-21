---
title: 'Hackers bypass SonicWall VPN MFA due to incomplete patching'
date: 2026-05-21
permalink: /posts/2026/05/21/hackers-bypass-sonicwall-vpn-mfa-due-to-incomplete-patching/
tags:
- veille-cyber
- bleepingcomp
---
### Contournement de l'authentification MFA sur SonicWall VPN

Des cyberattaquants exploitent une vulnérabilité dans les appliances SonicWall Gen6 pour contourner l'authentification multifacteur (MFA) et obtenir un accès initial aux réseaux internes. Les intrusions observées suggèrent le recours à des courtiers d'accès initial visant à déployer des ransomwares ou des outils de persistance (Cobalt Strike, techniques BYOVD). Une particularité inquiétante de cette attaque est que les journaux de connexion affichent un flux MFA normal, masquant ainsi le succès du contournement.

**Points clés :**
*   **Vulnérabilité critique :** La faille **CVE-2024-12802** permet aux attaquants de contourner le MFA en utilisant le format de connexion UPN (*User Principal Name*).
*   **Piège de la mise à jour :** Sur les appareils Gen6, l'installation du firmware ne suffit pas. Une reconfiguration manuelle du serveur LDAP est impérative pour neutraliser la menace.
*   **Indicateurs de compromission :** Surveiller les journaux pour le signal `sess=”CLI”` (indiquant une authentification automatisée), les ID d'événement 238 et 1080, ainsi que les connexions provenant d'infrastructures VPN/VPS suspectes.

**Vulnérabilités :**
*   **CVE-2024-12802 :** Défaut d'application du MFA lors de l'utilisation du format UPN pour l'authentification.

**Recommandations :**
1.  **Remédiation Gen6 :** Appliquer le firmware, puis supprimer et recréer manuellement la configuration LDAP en évitant l'utilisation du champ "userPrincipalName" (se référer à l'avis officiel de SonicWall pour les étapes détaillées).
2.  **Mise à jour Gen7/Gen8 :** La simple mise à jour du firmware suffit pour ces modèles.
3.  **Obsolescence :** Les appareils Gen6 ayant atteint leur fin de vie (*End-of-Life*) en avril 2024, leur remplacement par des équipements supportés est vivement préconisé.
4.  **Audit :** Examiner les journaux d'accès VPN à la recherche de comportements automatisés et vérifier la présence de privilèges d'administrateur local partagés sur les serveurs internes.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-bypass-sonicwall-vpn-mfa-due-to-incomplete-patching/){:target="_blank"}
