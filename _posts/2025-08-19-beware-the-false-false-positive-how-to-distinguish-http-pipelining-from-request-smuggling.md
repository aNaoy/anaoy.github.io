---
title: 'Beware the false false-positive: how to distinguish HTTP pipelining from request smuggling'
date: 2025-08-19
permalink: /posts/2025/08/19/beware-the-false-false-positive-how-to-distinguish-http-pipelining-from-request-smuggling/
tags:
- veille-cyber
- zerodaysfans
---
### La Nuance entre Réutilisation de Connexion HTTP et Vol de Requête

Il est fréquent de confondre les effets de la réutilisation de connexions HTTP (pipelining ou keep-alive) avec le vol de requête (request smuggling). Bien que la réutilisation de connexion puisse souvent mener à de faux positifs lors des tests, il existe des scénarios où elle est intrinsèquement liée à des vulnérabilités réelles.

**Points Clés :**

*   La réutilisation de connexions HTTP, où plusieurs requêtes sont envoyées sur la même connexion TCP/TLS, est un comportement normal du protocole HTTP/1.1.
*   Les preuves de concept de vol de requête qui ne fonctionnent *qu'avec* la réutilisation de connexion sont généralement des faux positifs, souvent observés avec des outils comme Turbo Intruder ou Burp Suite lorsqu'ils sont configurés pour la réutilisation.
*   Cependant, certains types de vulnérabilités, bien que liés au vol de requête, nécessitent la réutilisation de la connexion côté client pour être déclenchés.

**Vulnérabilités et Scénarios Connexes où la Réutilisation est Importante :**

*   **Vol de Requête Verrouillé sur Connexion (Connection-locked Request Smuggling) :** Dans ce cas, le serveur frontal ne réutilise la connexion montante que si la connexion client est réutilisée. Cela peut masquer une véritable vulnérabilité au vol de requête qui ne peut être exploitée qu'à travers la réutilisation de connexion côté client. Pour prouver son existence, on peut rechercher si une réponse HTTP/1 est imbriquée dans une réponse HTTP/2, ou utiliser des requêtes partielles. L'impact peut inclure le empoisonnement de cache, la révélation d'en-têtes internes (potentiellement menant à un contournement d'authentification), ou le contournement de contrôles de sécurité du serveur frontal.
*   **Attaques d'État de Connexion (Connection State Attacks) :** Ces attaques exploitent le fait que certains serveurs traitent la première requête sur une connexion différemment des suivantes. Bien que techniquement pas du vol de requête, leur impact est similaire au vol de requête verrouillé sur connexion. Un outil comme HTTP Request Smuggler propose une fonctionnalité de "connection-state probe" pour les identifier.
*   **Attaques de Désynchronisation Côté Client (Client-Side Desync Attacks) :** Dans ce scénario, la réutilisation de connexion est exploitable, mais avec une restriction majeure : la requête d'attaque doit pouvoir être initiée par le navigateur de la victime et être inter-domaines, ce qui empêche l'utilisation de techniques d'obfuscation d'en-têtes.

**Recommandations :**

*   Lors des tests de vol de requête, désactivez systématiquement la réutilisation de connexion lorsque cela est possible. Si l'attaque échoue alors, cela indique un faux positif lié à la réutilisation.
*   Si l'attaque ne fonctionne qu'avec la réutilisation de connexion, examinez si cela correspond à l'un des scénarios de vulnérabilités réelles mentionnés ci-dessus.
*   Pour prouver l'impact de vulnérabilités liées à la réutilisation, explorez le empoisonnement de cache, la révélation d'en-têtes via des gadgets de réflexion d'entrée, le contournement de contrôles de sécurité, ou la manipulation de l'en-tête `Host`.
*   L'utilisation d'extensions comme HTTP Hacker pour Burp Suite peut aider à visualiser le comportement de bas niveau des connexions HTTP.
*   Un outil personnalisé comme "Smuggling or pipelining?" peut aider à distinguer ces comportements.

---
[Source](https://portswigger.net/research/how-to-distinguish-http-pipelining-from-request-smuggling){:target="_blank"}
