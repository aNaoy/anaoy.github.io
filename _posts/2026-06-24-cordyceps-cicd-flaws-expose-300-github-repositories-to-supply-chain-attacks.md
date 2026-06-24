---
title: 'Cordyceps CI/CD Flaws Expose 300+ GitHub Repositories to Supply-Chain Attacks'
date: 2026-06-24
permalink: /posts/2026/06/24/cordyceps-cicd-flaws-expose-300-github-repositories-to-supply-chain-attacks/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité Cordyceps : Risques critiques pour la chaîne d'approvisionnement CI/CD

La faille « Cordyceps » désigne une classe de vulnérabilités dans les configurations CI/CD de GitHub, permettant à des utilisateurs non authentifiés de détourner des flux de travail automatisés. Plus de 300 dépôts open-source majeurs (Microsoft, Google, Apache, Cloudflare) ont été identifiés comme exploitables.

**Points clés :**
* **Mécanisme :** L'exploitation repose sur des configurations CI/CD permissives où des requêtes de fusion (*Pull Requests*) non fiables déclenchent des flux de travail privilégiés.
* **Impact :** Exécution de code arbitraire, vol de jetons d'authentification (GitHub App keys), usurpation d'identité et compromission de la chaîne d'approvisionnement logicielle.
* **Complexité :** Le problème ne provient pas d'un bug logiciel classique, mais d'une mauvaise composition des flux de travail, rendant la détection par les scanners standards difficile.

**Vulnérabilités :**
* Aucune CVE spécifique n'a été attribuée, car il s'agit d'une faiblesse systémique liée à la configuration et non à une faille logicielle isolée.
* **Exemples observés :** Exécution de code via des commentaires de PR (Apache Doris), nom de branche malveillant (Cloudflare Workers SDK) ou injection via des PR externes (Python Black).

**Recommandations :**
* **Auditer les permissions :** Restreindre strictement les permissions accordées aux flux de travail déclenchés par des PR provenant de contributeurs externes ou de branches forkees.
* **Isoler les environnements :** Ne jamais utiliser de jetons ayant des droits d'écriture ou des accès aux secrets dans des flux de travail exposés à des entrées non fiables.
* **Renforcer la validation :** Mettre en œuvre des politiques de validation manuelle pour les flux de travail critiques et éviter l'automatisation basée sur des données utilisateur (commentaires, noms de branche).
* **Gestion des secrets :** Utiliser des jetons à durée de vie limitée et suivre le principe du moindre privilège pour les clés d'application GitHub.

---
[Source](https://thehackernews.com/2026/06/cordyceps-cicd-flaws-expose-300-github.html){:target="_blank"}
