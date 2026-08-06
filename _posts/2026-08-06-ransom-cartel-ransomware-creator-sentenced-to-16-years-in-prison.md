---
title: 'Ransom Cartel ransomware creator sentenced to 16 years in prison'
date: 2026-08-06
permalink: /posts/2026/08/06/ransom-cartel-ransomware-creator-sentenced-to-16-years-in-prison/
tags:
- veille-cyber
- bleepingcomp
---
### Condamnation du créateur du ransomware « Ransom Cartel »

Maksim Silnikau, ressortissant biélorusse de 40 ans, a été condamné à 16 ans de prison aux États-Unis pour son rôle central dans le groupe cybercriminel « Ransom Cartel ». Actif entre 2021 et 2023, ce groupe a ciblé au moins 18 entreprises, causant plus de 6,7 millions de dollars de dommages et tentant d'extorquer 5,2 millions de dollars via des demandes de rançon.

**Points clés :**
*   **Modèle opérationnel :** Silnikau gérait une plateforme de « Ransomware-as-a-Service » (RaaS), recrutant des affiliés, fournissant des accès initiaux aux réseaux d'entreprises, supervisant le chiffrement des données et négociant les paiements.
*   **Techniques de blanchiment :** Utilisation intensive de mélangeurs de cryptomonnaies pour occulter la trace des fonds issus des extorsions.
*   **Liens avec REvil :** Le code du ransomware présentait des similitudes avec le célèbre logiciel malveillant REvil, suggérant une origine commune ou une utilisation détournée par un ancien membre.
*   **Parcours judiciaire :** Arrêté initialement en Espagne en 2023, Silnikau s'est enfui avant d'être recapturé à la frontière polonaise alors qu'il tentait de rejoindre la Biélorussie, menant finalement à son extradition vers les États-Unis.

**Vulnérabilités exploitées :**
L'article ne mentionne pas de CVE spécifiques, mais souligne que le groupe exploitait des accès aux réseaux compromis fournis par des courtiers en accès initial (Initial Access Brokers). Les vecteurs d'attaque reposaient sur :
*   L'utilisation d'identifiants volés pour l'intrusion initiale.
*   L'exploitation de failles logicielles non précisées pour le déploiement du chiffrement.

**Recommandations :**
Bien qu'aucune mesure technique spécifique ne soit détaillée, la nature de ces attaques impose des pratiques de cybersécurité rigoureuses pour se protéger contre les groupes RaaS :
*   **Gestion des accès :** Implémenter l'authentification multifacteur (MFA) pour neutraliser l'utilisation d'identifiants volés.
*   **Surveillance réseau :** Utiliser des outils de simulation de brèches et d'attaques (BAS) pour tester l'efficacité des solutions EDR/SIEM face aux mouvements latéraux des attaquants.
*   **Politique de sauvegarde :** Maintenir des sauvegardes immuables hors ligne afin de restaurer les systèmes sans céder aux demandes de rançon.
*   **Hygiène informatique :** Appliquer une politique stricte de mise à jour des systèmes pour corriger les vulnérabilités exploitées par les courtiers en accès initial.

---
[Source](https://www.bleepingcomputer.com/news/security/ransom-cartel-ransomware-creator-sentenced-to-16-years-in-prison/){:target="_blank"}
