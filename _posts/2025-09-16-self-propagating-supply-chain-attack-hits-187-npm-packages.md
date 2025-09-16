---
title: 'Self-propagating supply chain attack hits 187 npm packages'
date: 2025-09-16
permalink: /posts/2025/09/16/self-propagating-supply-chain-attack-hits-187-npm-packages/
tags:
- veille-cyber
- bleepingcomp
---
**Attaque par propagation virale sur npm : 187 paquets compromis**

Une campagne d'attaque de la chaîne d'approvisionnement logicielle, baptisée "Shai-Hulud", a affecté au moins 187 paquets du registre npm. Cette attaque se caractérise par un mécanisme d'auto-propagation qui cible d'autres paquets du même mainteneur.

Le processus malveillant télécharge les paquets, modifie leur fichier `package.json` pour y injecter un script `bundle.js`, réemballe l'archive et la republie. Ce script utilise ensuite l'outil légitime de scan de secrets TruffleHog pour rechercher des informations sensibles (clés API, mots de passe, jetons) sur l'hôte. Il tente de valider ces identifiants pour créer des workflows GitHub Actions non autorisés et exfiltrer les données vers un webhook prédéfini.

L'attaque initiale aurait débuté avec le paquet `@ctrl/tinycolor`, téléchargé plus de 2 millions de fois par semaine, et s'est étendue à des paquets publiés sous le namespace de CrowdStrike.

**Points clés :**

*   **Nature de l'attaque :** Chaîne d'approvisionnement logicielle, avec un composant d'auto-propagation viral.
*   **Cible :** Registre npm, affectant 187 paquets.
*   **Mécanisme :** Injection d'un script malveillant (`bundle.js`) dans les paquets, utilisant TruffleHog pour voler des secrets.
*   **Objectif :** Exfiltration de secrets (clés API, jetons, identifiants) via un webhook.
*   **Nom de code :** "Shai-Hulud", en référence aux vers de sable de Dune.
*   **Impact :** Potentiel d'infection de centaines de projets dépendants, y compris des projets d'envergure comme Google Gemini CLI.
*   **Contexte :** S'inscrit dans une série d'attaques récentes sur la chaîne d'approvisionnement logicielle (par ex. 's1ngularity').

**Vulnérabilités :**

Aucun numéro CVE spécifique n'est mentionné dans l'article, car l'attaque exploite la compromission des comptes de mainteneurs et l'injection de code malveillant dans les paquets, plutôt qu'une vulnérabilité technique spécifique dans le registre npm lui-même.

**Recommandations :**

*   Auditer les environnements et les journaux à la recherche de signes de compromission.
*   Rotation de tous les secrets et jetons CI/CD.
*   Vérifier les arbres de dépendances pour identifier les versions malveillantes.
*   Épingler les dépendances à des versions approuvées.
*   Limiter la portée des identifiants de publication.
*   Éviter d'installer les dernières versions de paquets suspects.

---
[Source](https://www.bleepingcomputer.com/news/security/self-propagating-supply-chain-attack-hits-187-npm-packages/){:target="_blank"}
