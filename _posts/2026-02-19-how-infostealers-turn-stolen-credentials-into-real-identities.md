---
title: 'How infostealers turn stolen credentials into real identities'
date: 2026-02-19
permalink: /posts/2026/02/19/how-infostealers-turn-stolen-credentials-into-real-identities/
tags:
- veille-cyber
- bleepingcomp
---
**La Transformation des Identifiants Volés en Identités Réelles par les Infostealers**

Les programmes malveillants de vol d'informations (infostealers) ont considérablement élargi leur portée au-delà de la simple collecte de noms d'utilisateur et de mots de passe. Ils ciblent désormais aussi bien les employés en entreprise que les utilisateurs sur leurs appareils personnels. L'analyse de plus de 90 000 lots de données volées par ces logiciels, représentant plus de 800 millions d'entrées, révèle comment ces informations sont agrégées et vendues pour être réutilisées dans diverses attaques. Ces données incluent non seulement les identifiants, mais aussi les cookies de navigateur, l'historique de navigation et des fichiers système locaux, permettant aux attaquants d'associer des données techniques à des utilisateurs réels, à leurs comportements et à leurs organisations.

Le risque majeur réside dans la facilité avec laquelle ces données permettent de relier plusieurs comptes et activités à une seule personne. La réutilisation des identifiants sur différents services, combinée aux noms d'utilisateur Windows et aux données d'activité, permet aux cybercriminels de passer d'une simple information d'identification compromise à l'identification complète d'un individu, de son employeur et potentiellement de son rôle. Cette convergence brouille la distinction entre identité personnelle et professionnelle, transformant une compromission sur un appareil personnel en un risque d'entreprise sérieux.

Les infostealers collectent des données provenant d'un large éventail de services, incluant des plateformes professionnelles (LinkedIn, GitHub, Microsoft Teams, Outlook, domaines d'entreprise) et personnelles (YouTube, Facebook). Ils accèdent également à des services sensibles comme des domaines gouvernementaux (IRS, Canada Revenue Agency) et des plateformes pour adultes, dont les données peuvent être utilisées à des fins d'extorsion. Paradoxalement, même les utilisateurs ayant une certaine connaissance de la sécurité, comme ceux accédant à des domaines tels que Shodan ou mil.gov, ne sont pas à l'abri.

L'efficacité persistante des infostealers s'explique par la combinaison de comportements courants à grande échelle : installation d'applications illicites, réutilisation de mots de passe entre comptes personnels et professionnels, et stockage des identifiants dans les navigateurs. Ces derniers fournissent un accès immédiat à des informations de grande valeur.

La mitigation de l'impact post-vol d'informations est cruciale. Une fois les données diffusées, il est essentiel de neutraliser leur réutilisation. La réutilisation des mots de passe est le principal levier d'exploitation. Des politiques de mots de passe plus robustes, favorisant des phrases de passe plus longues et une application continue, transforment la sécurité des mots de passe d'une configuration statique en une mesure de confinement active. Réduire la réutilisation et l'impact en aval des identifiants compromis est le moyen le plus efficace de briser les chaînes d'attaque initiées par les infostealers.

**Points Clés:**

*   Les infostealers ne se contentent plus de voler des identifiants, ils collectent des données permettant de reconstituer une identité complète.
*   La réutilisation des mots de passe est le principal facteur permettant aux attaquants d'exploiter les données volées sur des environnements professionnels.
*   Les données volées proviennent d'une multitude de services, allant des plateformes professionnelles aux sites gouvernementaux, augmentant ainsi le risque.
*   Même les comportements conscients en matière de sécurité ne protègent pas contre l'exposition, surtout lorsque les pratiques professionnelles ne sont pas étendues aux appareils personnels.
*   La neutralisation de la réutilisation des identifiants compromis est essentielle pour limiter l'impact des attaques par infostealers.

**Vulnérabilités:**

*   La réutilisation des mots de passe entre services personnels et professionnels est une vulnérabilité critique exploitée par les infostealers.
*   Le stockage des identifiants et des données de paiement dans les navigateurs constitue une cible de grande valeur.

**Recommandations:**

*   Mettre en place des politiques de mots de passe robustes, encourageant l'utilisation de phrases de passe longues.
*   Scanner continuellement les identifiants actifs (par exemple, dans Active Directory) par rapport aux bases de données de mots de passe compromis connus.
*   Bloquer l'utilisation ou la réutilisation des identifiants déjà exposés, même s'ils respectent techniquement les politiques de complexité.
*   Promouvoir l'adoption de pratiques de sécurité cohérentes entre les environnements personnels et professionnels.

---
[Source](https://www.bleepingcomputer.com/news/security/how-infostealers-turn-stolen-credentials-into-real-identities/){:target="_blank"}
