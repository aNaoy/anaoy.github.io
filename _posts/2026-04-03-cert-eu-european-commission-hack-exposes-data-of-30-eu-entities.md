---
title: 'CERT-EU: European Commission hack exposes data of 30 EU entities'
date: 2026-04-03
permalink: /posts/2026/04/03/cert-eu-european-commission-hack-exposes-data-of-30-eu-entities/
tags:
- veille-cyber
- bleepingcomp
---
### Violation de données à la Commission européenne via AWS

Le CERT-EU a confirmé qu'une intrusion dans l'environnement cloud Amazon Web Services (AWS) de la Commission européenne a conduit à l'exfiltration de données sensibles concernant 29 entités de l'Union européenne et 42 services internes. L'attaque a été attribuée au groupe cybercriminel « TeamPCP », tandis que les données volées (environ 90 Go compressés) ont été publiées sur le dark web par le groupe d'extorsion « ShinyHunters ».

**Points clés :**
* **Origine de l'intrusion :** Utilisation d'une clé d'API AWS compromise, initialement dérobée lors de l'attaque par chaîne d'approvisionnement visant l'outil *Trivy*.
* **Chronologie :** L'intrusion a débuté le 10 mars, mais n'a été détectée par le centre d'opérations de sécurité que le 24 mars, soit cinq jours après l'accès initial.
* **Impact :** Vol de dizaines de milliers de fichiers contenant des noms, des noms d'utilisateur, des adresses e-mail et le contenu de communications électroniques (dont des notifications « bounce-back » contenant des informations soumises par les utilisateurs).
* **Modus Operandi :** Les attaquants ont utilisé l'outil *TruffleHog* pour rechercher des secrets supplémentaires et ont créé une nouvelle clé d'accès rattachée à un utilisateur existant pour échapper à la détection.

**Vulnérabilités :**
* Compromission de clés d'API (Secrets AWS) via une attaque par chaîne d'approvisionnement (Supply-Chain Attack).
* Absence de détection en temps réel des abus d'API et des comportements réseau anormaux dans l'environnement cloud.

**Recommandations :**
* **Gestion des secrets :** Éviter le stockage en dur des clés API et mettre en place une rotation régulière et automatique des secrets.
* **Surveillance proactive :** Renforcer la surveillance des journaux d'audit AWS (CloudTrail) pour détecter rapidement la création de nouvelles clés d'accès ou l'utilisation inhabituelle d'identifiants existants.
* **Principe du moindre privilège :** Restreindre strictement les droits des clés API et isoler les comptes cloud pour limiter le mouvement latéral en cas de compromission.
* **Détection des menaces :** Utiliser des outils d'analyse de comportement (UEBA) pour identifier les activités anormales, comme le balayage de secrets, indépendamment des alertes de sécurité standard.

---
[Source](https://www.bleepingcomputer.com/news/security/cert-eu-european-commission-hack-exposes-data-of-30-eu-entities/){:target="_blank"}
