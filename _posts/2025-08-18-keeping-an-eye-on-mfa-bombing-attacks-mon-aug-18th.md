---
title: 'Keeping an Eye on MFA-Bombing Attacks, (Mon, Aug 18th)'
date: 2025-08-18
permalink: /posts/2025/08/18/keeping-an-eye-on-mfa-bombing-attacks-mon-aug-18th/
tags:
- veille-cyber
- sans-isc
---
### Cyberattaques par Bombardement MFA : Analyse et Défense

Des attaques de type "MFA-bombing" visent à submerger les utilisateurs avec des demandes de validation multifacteur (MFA) dans l'espoir qu'ils finissent par en accepter une pour faire cesser le flux. Une fois que des identifiants compromis sont utilisés, l'attaquant peut potentiellement accéder à des ressources, escalader ses privilèges sur le réseau interne, ou utiliser ces identifiants sur d'autres services exposés sur Internet.

#### Points Clés :

*   **Le principe du MFA-bombing :** Les attaquants exploitent le comportement humain en submergeant les utilisateurs de notifications MFA. La fatigue de ces alertes peut amener un utilisateur à approuver une demande frauduleuse.
*   **Vecteurs d'attaque :** Outre le bombardement direct, les attaquants peuvent se faire passer pour le support technique afin d'inciter la victime à approuver la demande.
*   **Conséquences d'un succès :** Si une attaque réussit, l'attaquant peut accéder aux données du site compromis, pivoter vers le réseau interne, collecter d'autres identifiants, et potentiellement prendre le contrôle total de l'environnement.
*   **Analyse des journaux :** Les journaux de connexion (par exemple, sur `account.microsoft.com` pour les utilisateurs individuels ou via le portail Azure pour les administrateurs) sont cruciaux pour identifier ces tentatives d'accès.

#### Vulnérabilités :

L'article ne mentionne pas de CVE spécifiques, mais souligne les vulnérabilités suivantes :

*   **Ingénierie sociale :** Exploitation de la crédulité des utilisateurs pour les amener à approuver des demandes MFA frauduleuses.
*   **Manque de clarté dans les outils de sécurité :** La difficulté à retrouver l'historique des connexions et à visualiser les tentatives d'attaque pour les utilisateurs individuels.
*   **Pratiques de stockage d'identifiants obsolètes :** Des ressources web anciennes stockant potentiellement des mots de passe en clair ou utilisant un chiffrement réversible, et s'authentifiant directement sur l'Active Directory sans MFA pour des raisons de "performance".

#### Recommandations :

*   **Vérifier l'historique des connexions :** Les utilisateurs doivent régulièrement consulter leur historique de connexion via des portails comme `mysignins.microsoft.com` pour identifier toute activité suspecte.
*   **Surveillance administrative des journaux :** Les administrateurs doivent utiliser des outils comme le portail Azure (`portal.azure.com` -> Identity Protection -> Dashboard -> Risk Detections) pour surveiller les tentatives d'accès et les activités suspectes des utilisateurs.
*   **Améliorer l'accessibilité des données :** Les administrateurs devraient chercher des moyens d'accéder aux journaux de connexion de manière centralisée, idéalement via des API ou des scripts pour les intégrer dans un SIEM.
*   **Sensibilisation des utilisateurs :** Informer les utilisateurs sur les attaques par MFA-bombing et leur apprendre à reconnaître les demandes suspectes et à ne jamais approuver les notifications MFA qu'ils n'ont pas initiées.
*   **Sécurisation des ressources web :** S'assurer que toutes les ressources web, en particulier celles connectées à l'Active Directory, implémentent le MFA et utilisent des pratiques de stockage d'identifiants modernes et sécurisées.

---
[Source](https://isc.sans.edu/diary/rss/32208){:target="_blank"}
