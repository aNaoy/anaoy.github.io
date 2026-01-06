---
title: 'Top 10 web hacking techniques of 2025: call for nominations'
date: 2026-01-06
permalink: /posts/2026/01/06/top-10-web-hacking-techniques-of-2025-call-for-nominations/
tags:
- veille-cyber
- zerodaysfans
---
### Technologies Web et Techniques d'Attaque : Appel à Contributions pour 2025

La communauté de la cybersécurité est invitée à soumettre des recherches sur les techniques de piratage web les plus innovantes et réutilisables de 2024. L'objectif est de distinguer des méthodes qui vont au-delà de la simple identification de vulnérabilités individuelles (comme Log4Shell) pour mettre en lumière des approches sous-jacentes permettant de compromettre divers systèmes (par exemple, l'injection JNDI). Les améliorations de classes d'attaques connues, comme l'exploitation de XXE avec des fichiers DTD locaux, sont également les bienvenues.

Le processus de sélection inclut une période de collecte des nominations, un vote communautaire pour établir une liste restreinte, et un vote d'experts pour déterminer le classement final des dix techniques. Les soumissions doivent inclure un lien vers la recherche et une brève description de sa nouveauté. Les discussions se poursuivent sur Discord.

**Points Clés :**

*   Appel à contributions pour identifier les dix techniques de piratage web les plus significatives de 2024.
*   Mise en avant de techniques innovantes et réutilisables plutôt que de vulnérabilités isolées.
*   Processus de sélection en plusieurs étapes : nomination, vote communautaire, vote d'experts.
*   Les nominations peuvent concerner des techniques inédites ou des améliorations d'attaques existantes.

**Quelques Exemples de Recherches Nominées (et techniques associées) :**

*   **Exploitation de conditions de concurrence (race conditions) dans Next.js** : Permet de contourner des correctifs et d'empoisonner le cache pour des attaques XSS.
*   **Interprétation ambiguë de formats dans les analyseurs Go** : Exploitation des différences entre JSON et XML pour contourner l'authentification et l'autorisation.
*   **Désynchronisation de requêtes HTTP/1.1 via des subtilités de la gestion "Expect"** : Permet le détournement de files d'attente de réponses et le piratage de contenu inter-locataires.
*   **Attaques par DOM Clobbering et injection dans les attributs d'iframe** : Contournement des protections comme DOMPurify pour obtenir des attaques XSS.
*   **Désynchronisation inter-protocoles au niveau applicatif ("Opossum Attack")** : Manipulation des flux de requêtes/réponses via des mises à niveau TLS opportunistes.
*   **Bypass de l'authentification SAML via la canalisation de la validation** : Exploitation des incohérences entre la vérification de signature et le traitement des assertions.
*   **Piratage de requêtes HTTP via des terminateurs de ligne ambigus dans les corps chunkés** : Nouvelles méthodes d'attaques par contournement de la logique de parsing, indépendantes de la confusion Content-Length/Transfer-Encoding.
*   **Piratage de WebSockets inter-sites (CSWSH)** : Contournement des protections CSRF via GraphQL sur WebSockets et accès aux services sur réseaux privés.
*   **Clickjacking SVG avancé** : Lecture de pixels et interaction multi-étapes via les pipelines de filtres SVG pour une exfiltration de données.
*   **Bypass de CSP (Content Security Policy) basé sur un nonce via le cache disque** : Réutilisation d'un nonce CSP divulgué par le biais du cache pour injecter du contenu.
*   **Nouvelle technique SSRF impliquant des boucles de redirection HTTP** : Exploitation des variations de codes de statut dans les boucles de redirection pour révéler la chaîne complète de requêtes et la réponse finale.
*   **Exploitation de la normalisation Unicode** : Contournement des validations en exploitant les incohérences de normalisation Unicode.
*   **Piratage des applications .NET Framework via des proxys HTTP Client et WSDL ("SOAPwn")** : Exploitation de la génération de proxys SOAP pour des écritures de fichiers arbitraires et le relais NTLM, menant à une exécution de code à distance.
*   **Forçage du "Quirks Mode" avec des avertissements PHP et exfiltration CSS sans requêtes réseau** : Exploitation des avertissements PHP pour contourner les restrictions MIME des feuilles de style et exfiltrer des données sous CSP.
*   **Fuites via ORM (Object-Relational Mapping)** : Exploitation de failles dans les expressions de filtre et confusion de types pour contourner la validation et l'authentification.

**Recommandations :**

*   Les chercheurs sont encouragés à soumettre des recherches qui démontrent des techniques nouvelles et pratiques pouvant être appliquées à différents contextes.
*   Il est recommandé de consulter les listes des années précédentes pour comprendre le type de recherche valorisé.
*   Pour être informé des étapes de vote, il est conseillé de suivre les comptes de recherche sur les réseaux sociaux (@PortSwiggerRes).

---
[Source](https://portswigger.net/research/top-10-web-hacking-techniques-of-2025-nominations-open){:target="_blank"}
