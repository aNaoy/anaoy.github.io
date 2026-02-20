---
title: 'How infostealers turn stolen credentials into real identities'
date: 2026-02-20
permalink: /posts/2026/02/20/how-infostealers-turn-stolen-credentials-into-real-identities/
tags:
- veille-cyber
- bleepingcomp
---
## L'évolution des infostealers : de simples identifiants à des identités numériques complètes

Les logiciels malveillants de type "infostealer" ont considérablement élargi leur champ d'action, allant bien au-delà du simple vol de noms d'utilisateur et de mots de passe. Ces dernières années ont vu une intensification des campagnes ciblant indistinctement les employés d'entreprise et les particuliers sur leurs appareils personnels. Les infostealers collectent systématiquement des identifiants, des données de session et des informations sur l'activité des utilisateurs. Les données ainsi agrégées sont vendues par des intermédiaires spécialisés, puis utilisées dans des attaques visant à la fois les environnements personnels et professionnels.

Une analyse de plus de 90 000 ensembles de données provenant d'infostealers a révélé que ces outils permettent désormais aux attaquants de corréler des données techniques avec des individus réels, leurs organisations et leurs habitudes. Cette convergence transforme un simple identifiant compromis en une mine d'informations permettant d'établir une identité numérique complète. L'exposition de noms d'utilisateur réutilisés sur divers services, des informations de profil, des données de session et des historiques d'activité facilite l'identification d'une personne, de son employeur et de son rôle potentiel au sein d'une organisation. Cela brouille la frontière entre vie privée et vie professionnelle, permettant à une compromission initiale sur un appareil personnel de se propager rapidement aux environnements d'entreprise.

Les données compromises incluent une vaste gamme de services, allant des plateformes professionnelles comme LinkedIn, GitHub et Microsoft Teams, aux réseaux sociaux comme YouTube et Facebook, en passant par des services sensibles tels que des plateformes gouvernementales (IRS, Canada Revenue Agency) et des sites à contenu adulte. Ces informations permettent des campagnes de phishing ciblées, des attaques d'ingénierie sociale et une priorisation des accès pour pénétrer plus profondément dans les réseaux d'entreprise. L'exploitation de données provenant de plateformes adultes peut également être utilisée à des fins d'extorsion. Il est à noter que même des environnements techniquement conscients, comme ceux utilisant Shodan ou des domaines .gov, ne sont pas immunisés, soulignant que les bonnes pratiques de sécurité ne s'étendent pas toujours aux systèmes personnels, mais que ces derniers peuvent tout de même représenter un risque pour les entreprises.

L'efficacité persistante des infostealers repose sur des comportements courants répétés à grande échelle : installation de logiciels provenant de sources illicites, réutilisation des mots de passe entre comptes personnels et professionnels, et confiance dans le stockage des identifiants par les navigateurs. Le vol de ces informations de navigateur est particulièrement précieux pour les attaquants.

Une fois les données des infostealers collectées et diffusées, la mitigation devient cruciale. La réutilisation des mots de passe est un vecteur majeur par lequel les attaquants exploitent ces données. Les identifiants volés sur des appareils personnels sont souvent testés contre des environnements professionnels, des services cloud et des systèmes d'accès à distance, avec succès même si les mots de passe respectent les exigences de complexité standard. Interrompre cette réutilisation réduit la valeur opérationnelle des ensembles de données d'infostealers et raccourcit leur fenêtre d'exploitation. L'adoption de politiques de mots de passe plus robustes, favorisant des phrases de passe longues et un contrôle continu, transforme la sécurité des mots de passe d'une simple configuration statique en une mesure de confinement active.

### Points Clés :

*   **Évolution des infostealers :** Ils ne se limitent plus aux identifiants, mais collectent des données de session, l'activité de l'utilisateur, et des fichiers système pour construire des identités numériques complètes.
*   **Corrélation des données :** Les dump d'infostealers permettent de lier des données techniques à des personnes réelles, leurs organisations et leurs comportements, même à travers la réutilisation de mots de passe.
*   **Risque accru :** Une compromission sur un appareil personnel peut rapidement entraîner un risque d'entreprise significatif.
*   **Large éventail de services ciblés :** Des plateformes professionnelles aux réseaux sociaux, en passant par des services gouvernementaux et des sites à contenu adulte.
*   **Causes de l'efficacité :** Comportements courants des utilisateurs comme la réutilisation de mots de passe et la confiance dans le stockage des identifiants par les navigateurs.
*   **Impact de la réutilisation des identifiants :** Les identifiants compromis sur des appareils personnels sont systématiquement testés contre des environnements d'entreprise, souvent avec succès.

### Vulnérabilités / Risques :

*   **Réutilisation de mots de passe (Password Reuse) :** Permet aux attaquants de passer d'un compte compromis à un autre, y compris dans des environnements d'entreprise.
*   **Stockage d'identifiants par les navigateurs :** Offre un accès immédiat à des informations précieuses pour les attaquants.
*   **Manque d'extension des bonnes pratiques de sécurité personnelles aux systèmes d'entreprise.**

### Recommandations :

*   **Arrêter la réutilisation des mots de passe :** Cela réduit directement la valeur opérationnelle des données d'infostealers.
*   **Mettre en place des politiques de mots de passe plus robustes :** Soutenir des phrases de passe plus longues et assurer un contrôle continu.
*   **Scanner activement Active Directory :** Vérifier en continu les identifiants par rapport à des bases de données de mots de passe compromis connus, plutôt que de se limiter à la création ou à la réinitialisation des mots de passe.
*   **Éduquer les utilisateurs :** Sensibiliser aux risques liés à l'installation de logiciels suspects et à la réutilisation des identifiants.

---
[Source](https://www.bleepingcomputer.com/news/security/how-infostealers-turn-stolen-credentials-into-real-identities/){:target="_blank"}
