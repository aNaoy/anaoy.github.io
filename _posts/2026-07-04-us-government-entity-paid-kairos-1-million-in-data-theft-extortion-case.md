---
title: 'U.S. Government Entity Paid Kairos $1 Million in Data-Theft Extortion Case'
date: 2026-07-04
permalink: /posts/2026/07/04/us-government-entity-paid-kairos-1-million-in-data-theft-extortion-case/
tags:
- veille-cyber
- hackernews
---
### Extorsion par le vol de données : Le cas Kairos

Une entité gouvernementale américaine (probablement le comté d'Union, dans l'Ohio) a versé environ 1 million de dollars en cryptomonnaie au groupe cybercriminel « Kairos » pour empêcher la fuite de données sensibles dérobées. 

**Points clés :**
* **Changement de paradigme :** Contrairement au ransomware classique, Kairos ne chiffre pas les systèmes. Le groupe se contente d'exfiltrer les données et d'extorquer la victime sous la menace de les publier.
* **Négociation :** Le groupe a initialement réclamé 3 millions de dollars pour plus de 2 To de données, avant d'accepter 1 million de dollars.
* **Absence de garantie :** Le paiement ne garantit en rien la suppression réelle des données, la preuve fournie par les attaquants ne confirmant que la possession initiale des fichiers.
* **Traçabilité :** Les fonds ont été retracés vers des plateformes d'échange (Bybit, OKX) et des services russes (BELQI), soulignant la difficulté de récupérer les fonds ou d'identifier les auteurs.

**Vulnérabilités exploitées :**
* Bien qu'aucune CVE spécifique ne soit mentionnée, l'article souligne l'utilisation de **mots de passe faibles/devinés** pour accéder au réseau, mettant en évidence un manque critique d'authentification forte.

**Recommandations de sécurité :**
* **Authentification multi-facteurs (MFA) :** Mesure indispensable pour contrer les accès par compromission de mots de passe.
* **Surveillance proactive :** Détecter les tentatives de connexion répétées et les transferts sortants de volumes de données inhabituels.
* **Segmentation réseau :** Isoler les données critiques (juridiques, RH, citoyens) du reste du réseau pour limiter l'impact en cas d'intrusion.
* **Plan de communication :** Préparer une stratégie de gestion de crise et de communication publique en amont.
* **Politique de non-paiement :** Considérer les promesses de suppression de données par des criminels comme nulles et non avenues, le paiement ne garantissant aucune protection contre une divulgation future.

---
[Source](https://thehackernews.com/2026/07/us-government-entity-paid-kairos-group.html){:target="_blank"}
