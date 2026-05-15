---
title: 'TeamPCP hackers advertise Mistral AI code repos for sale'
date: 2026-05-15
permalink: /posts/2026/05/15/teampcp-hackers-advertise-mistral-ai-code-repos-for-sale/
tags:
- veille-cyber
- bleepingcomp
---
### Cyberattaque par chaîne d'approvisionnement chez Mistral AI

Le groupe de hackers « TeamPCP » menace de divulguer environ 450 dépôts de code source appartenant à Mistral AI, réclamant 25 000 dollars pour empêcher la publication des données. Cette brèche fait suite à l'attaque dite « Mini Shai-Hulud », une compromission de la chaîne d'approvisionnement logicielle ayant touché plusieurs entreprises technologiques.

**Points clés :**
*   **Origine de l'incident :** L'attaque a été initiée par le détournement de paquets logiciels via les registres npm et PyPI (attaque sur TanStack), utilisant des identifiants CI/CD compromis.
*   **Impact limité :** Mistral AI précise que la compromission se limite à certains kits de développement (SDK) et qu'aucune donnée utilisateur, service hébergé ou environnement de recherche critique n'a été exposé.
*   **Mode opératoire :** Les attaquants ciblent les environnements de développement locaux des ingénieurs pour infiltrer les systèmes.
*   **Phénomène d'ampleur :** Des entreprises comme OpenAI ont également été touchées par cette même campagne d'attaque via TanStack, entraînant le vol de certains identifiants internes.

**Vulnérabilités :**
*   Compromission de la chaîne d'approvisionnement logicielle (Supply-Chain Attack).
*   Vol d'identifiants CI/CD et de certificats de signature de code.
*   Infection de terminaux de développement via des paquets tiers malveillants.
*   *Note : Aucune CVE spécifique n'est associée à cet incident, car il s'agit d'une attaque visant la confiance envers les paquets open source.*

**Recommandations :**
*   **Rotation des accès :** Révoquer et renouveler systématiquement les identifiants CI/CD, les clés API et les certificats de signature de code exposés.
*   **Sécurisation des terminaux :** Renforcer la sécurité des postes de travail des développeurs et surveiller étroitement les interactions avec les registres de dépendances externes.
*   **Gestion des dépendances :** Auditer les paquets open source utilisés dans les projets et restreindre l'usage de bibliothèques non vérifiées.
*   **Veille de sécurité :** Mettre à jour immédiatement les logiciels et outils de développement (ex: applications desktop) conformément aux recommandations de sécurité des éditeurs concernés.

---
[Source](https://www.bleepingcomputer.com/news/security/teampcp-hackers-advertise-mistral-ai-code-repos-for-sale/){:target="_blank"}
