---
title: 'PhantomRaven attack floods npm with credential-stealing packages'
date: 2025-10-29
permalink: /posts/2025/10/29/phantomraven-attack-floods-npm-with-credential-stealing-packages/
tags:
- veille-cyber
- bleepingcomp
---
## Campagne PhantomRaven : Vol de Identifiants via des Paquets NPM Malveillants

Une campagne active, nommée "PhantomRaven", cible les développeurs en distribuant des paquets npm conçus pour dérober des jetons d'authentification, des secrets CI/CD et des identifiants GitHub. Lancée en août, cette campagne a vu le déploiement de 126 paquets npm ayant généré plus de 86 000 téléchargements.

Les paquets malveillants imitent des projets légitimes et exploitent souvent des recommandations générées par l'IA ("slopsquatting"), où des assistants IA suggèrent des noms de paquets inexistants mais qui paraissent authentiques. Certains de ces paquets usurpent l'identité d'outils GitLab ou Apache.

### Points Clés de l'Attaque :

*   **Dépendances Dynamiques à Distance (RDD)** : Les paquets déclarent initialement zéro dépendance, mais téléchargent et exécutent des charges utiles malveillantes depuis des URL externes lors de l'installation (`npm install`), sans nécessiter d'interaction utilisateur.
*   **Profilage et Vol d'Informations** : La charge utile récupérée analyse l'environnement de la victime à la recherche d'adresses e-mail et, surtout, de jetons pour NPM, GitHub Actions, GitLab, Jenkins et CircleCI.
*   **Attaques de Chaîne d'Approvisionnement** : Les jetons volés peuvent permettre aux attaquants d'introduire des modifications malveillantes dans d'autres projets, ouvrant la voie à des attaques de chaîne d'approvisionnement.
*   **Évasion de Détection** : L'utilisation de RDD rend l'analyse statique difficile, permettant une évasion prolongée des défenses.
*   **Méthodes d'Exfiltration** : Les données sont exfiltrées via des requêtes HTTP GET (données dans l'URL), HTTP POST (données JSON) ou une connexion WebSocket.

### Vulnérabilités :

L'article ne mentionne pas de CVE spécifiques pour cette campagne. Les vulnérabilités exploitées sont inhérentes à la confiance accordée aux paquets issus de dépôts publics et à la manière dont les développeurs peuvent être induits en erreur, notamment par des recommandations IA ou des noms de paquets similaires.

### Recommandations :

*   Vérifier scrupuleusement la légitimité des paquets npm et s'assurer qu'ils proviennent de fournisseurs réputés.
*   Éviter de se fier aveuglément aux suggestions de paquets provenant d'IA génératives.
*   Double-vérifier les résultats de recherche de paquets pour distinguer les projets authentiques des imitations ou des projets typosquattés.

---
[Source](https://www.bleepingcomputer.com/news/security/phantomraven-attack-floods-npm-with-credential-stealing-packages/){:target="_blank"}
