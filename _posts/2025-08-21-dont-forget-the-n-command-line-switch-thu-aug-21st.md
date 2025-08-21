---
title: 'Dont Forget The "-n" Command Line Switch, (Thu, Aug 21st)'
date: 2025-08-21
permalink: /posts/2025/08/21/dont-forget-the-n-command-line-switch-thu-aug-21st/
tags:
- veille-cyber
- sans-isc
---
### L'importance de la résolution DNS inversée pour la discrétion

L'utilisation de la ligne de commande (CLI) est courante pour les investigations de sécurité grâce à sa puissance. De nombreux outils d'analyse de réseau et de logs, tels que `tcpdump`, `tshark`, `nethogs`, `nmap`, et bien d'autres, permettent de traiter des données. Une option fréquemment trouvée est `-n`, qui désactive la résolution DNS des adresses IP en noms de domaine complets (FQDN).

**Le risque de la résolution DNS :**

Lorsque les outils tentent de convertir des adresses IP en FQDN, si le système DNS gérant les enregistrements PTR (Pointer) est contrôlé par un attaquant, cela peut révéler qu'une investigation est en cours. Certains fournisseurs d'accès à Internet (FAI) délèguent la gestion des enregistrements PTR à leurs clients. Ces clients peuvent ainsi enregistrer les tentatives de résolution des enregistrements `in-addr.arpa`.

Une requête DNS inversée, comme celle effectuée avec `dig -x 23.30.39.252 @192.168.254.8`, peut générer des logs sur le serveur DNS. Ces logs indiquent l'adresse IP interrogée et l'adresse IP de la source de la requête. Cela permettrait à un attaquant de savoir que son infrastructure est examinée et potentiellement de connaître l'adresse IP de l'analyste.

De plus, tenter de résoudre des noms de domaine peut également être risqué. Si un attaquant contrôle le domaine principal, il peut détecter les tentatives de résolution, exposant ainsi les investigateurs.

**Points clés :**

*   De nombreux outils CLI désactivent la résolution DNS des adresses IP avec l'option `-n`.
*   La résolution DNS inversée des adresses IP peut alerter les attaquants si la zone DNS est sous leur contrôle.
*   Les FAI peuvent déléguer la gestion des enregistrements PTR, permettant aux clients de loguer les requêtes.
*   L'analyste peut être identifié par son adresse IP lors de ces requêtes.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans l'article. Le risque réside dans la conception même de la résolution DNS et la possibilité pour un attaquant de contrôler les zones DNS inversées.

**Recommandations :**

*   Utiliser l'option `-n` (ou son équivalent) avec les outils d'analyse réseau et de logs pour désactiver la résolution DNS des adresses IP et maintenir la discrétion lors des investigations.
*   Envisager l'utilisation de systèmes dédiés ou anonymes pour mener des investigations afin de masquer son adresse IP d'origine.
*   Être prudent lors de la résolution de noms de domaine suspects, car cela peut révéler une activité d'investigation à un attaquant.

---
[Source](https://isc.sans.edu/diary/rss/32220){:target="_blank"}
