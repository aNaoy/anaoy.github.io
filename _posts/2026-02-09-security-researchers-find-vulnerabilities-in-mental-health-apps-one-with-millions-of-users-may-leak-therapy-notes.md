---
title: 'Security Researchers Find Vulnerabilities in Mental Health Apps; One With Millions of Users May Leak Therapy Notes'
date: 2026-02-09
permalink: /posts/2026/02/09/security-researchers-find-vulnerabilities-in-mental-health-apps-one-with-millions-of-users-may-leak-therapy-notes/
tags:
- veille-cyber
- zerodaysfans
---
**Fissures de sécurité dans les applications de santé mentale : risque d'exfiltration de données sensibles**

Des chercheurs en sécurité ont découvert des vulnérabilités critiques dans plusieurs applications populaires de santé mentale, certaines comptant des millions d'utilisateurs. Ces failles, qui affectent des applications utilisées dans des programmes de santé étatiques, soutenues par des investissements majeurs et des essais cliniques reconnus, pourraient permettre à des applications malveillantes sur le même appareil d'accéder à des données extrêmement sensibles.

Le mécanisme d'attaque exploite le système de communication entre les applications Android. Des applications vulnérables diffusent des informations sans cibler de destinataire spécifique, permettant ainsi à d'autres applications, y compris celles conçues dans l'intention de nuire, de s'enregistrer comme écouteurs et d'intercepter ces données. Un scénario réaliste implique qu'une application apparemment inoffensive, comme une calculatrice, puisse subtilement capturer le contenu des conversations d'une application de santé mentale, y compris les états d'âme exprimés et les notes thérapeutiques.

Ces données personnelles, incluant des détails sur l'anxiété, la dépression, les traumatismes et les addictions, représentent une nouvelle cible de valeur pour les cybercriminels. Le marché des applications de santé mentale étant en pleine expansion, l'ampleur du problème est potentiellement considérable, d'autant plus que ces applications ne sont pas toujours couvertes par les réglementations protégeant les données de santé traditionnelles.

**Points clés :**

*   Des vulnérabilités ont été découvertes dans plusieurs applications populaires de santé mentale, avec des dizaines de millions de téléchargements cumulés.
*   Ces failles peuvent permettre l'interception de données sensibles, y compris les conversations avec des thérapeutes IA et les journaux de suivi de l'humeur.
*   Les données de santé mentale sont particulièrement précieuses sur le dark web, dépassant la valeur des informations de carte de crédit.
*   Le mécanisme d'attaque repose sur la diffusion non sécurisée de données via les "intents" Android.
*   Le marché des applications de santé mentale est en forte croissance, accentuant les risques potentiels.
*   Historiquement, des cas de piratage d'applications de santé mentale ont eu des conséquences dévastatrices.

**Vulnérabilités :**

*   Non spécifié par CVE dans l'article, mais le défaut principal réside dans la diffusion non sécurisée de données via les "intents" par certaines applications, permettant à d'autres applications d'y accéder sans autorisation.

**Recommandations :**

*   Il n'y a pas de recommandations spécifiques citées dans l'article, au-delà de la mise en évidence de la nécessité de renforcer la sécurité mobile. Les chercheurs n'ont pas divulgué les détails techniques pour permettre aux développeurs de corriger les failles avant qu'elles ne soient exploitées à grande échelle.

---
[Source](https://blog.oversecured.com/Security-researchers-find-vulnerabilities-in-mental-health-apps/){:target="_blank"}
