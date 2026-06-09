---
title: 'French govt messaging service breached in account hijacking attack'
date: 2026-06-09
permalink: /posts/2026/06/09/french-govt-messaging-service-breached-in-account-hijacking-attack/
tags:
- veille-cyber
- bleepingcomp
---
### Intrusion sur la messagerie gouvernementale Tchap

La plateforme de messagerie sécurisée Tchap, utilisée par les agents de l'État français, a subi une violation de données suite à la compromission d'un compte utilisateur. La DINUM a identifié et bloqué le compte source de l'attaque, tout en alertant la CNIL et les utilisateurs. Une enquête est en cours pour déterminer l'ampleur exacte des données exfiltrées.

**Points clés :**
*   **Vecteur d'attaque :** L'assaillant affirme avoir utilisé une technique d'ingénierie sociale pour compromettre un compte valide sur l'un des serveurs (shard) de l'Éducation nationale.
*   **Données exposées :** Selon le pirate, plus de 13,5 Go de documents/médias, 650 000 messages et des métadonnées concernant 73 000 comptes auraient été compromis.
*   **Vulnérabilité alléguée :** Le pirate prétend qu'il est possible de télécharger les fichiers partagés sur la plateforme sans authentification via leurs URL directes, et mentionne la découverte d'identifiants LDAP codés en dur dans un script PowerShell.
*   **Aucune CVE n'est associée à cet incident**, celui-ci reposant sur une compromission de compte et des faiblesses logicielles potentielles de conception.

**Recommandations :**
*   **Respect des usages :** Ne jamais échanger d'informations sensibles, personnelles ou confidentielles dans les salons de discussion publics, car ils ne sont pas chiffrés.
*   **Vigilance accrue :** Sensibiliser les utilisateurs aux risques d'ingénierie sociale visant à obtenir des accès aux comptes professionnels.
*   **Sécurité technique :** La DINUM et l'ANSSI doivent impérativement auditer la gestion des jetons d'accès aux fichiers (média) pour empêcher le téléchargement sans autorisation, ainsi que vérifier l'exposition d'identifiants (LDAP/secrets) dans les scripts internes.

---
[Source](https://www.bleepingcomputer.com/news/security/french-govt-messaging-service-breached-in-account-hijacking-attack/){:target="_blank"}
