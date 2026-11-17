---
title: 'Hackers Found a Way Around GitHub SHA Pinning. This Webinar Explains How to Close the Gap'
date: 2026-11-17
permalink: /posts/2026/11/17/hackers-found-a-way-around-github-sha-pinning-this-webinar-explains-how-to-close-the-gap/
tags:
- veille-cyber
- hackernews
---
### Les limites critiques du SHA Pinning dans GitHub Actions

Le "SHA pinning" (verrouillage par empreinte numérique) est devenu une pratique standard pour sécuriser la chaîne d'approvisionnement logicielle, mais il ne constitue plus une défense suffisante. Des attaquants exploitent désormais la structure des dépôts GitHub pour injecter du code malveillant via des forks, rendant ces compromissions invisibles pour les équipes qui se reposent uniquement sur le pinning.

**Points clés :**
*   **Immuabilité vs Provenance :** Le SHA garantit que le code n'a pas changé, mais ne prouve pas qui a écrit le code ou s'il provient du dépôt officiel.
*   **Tactique des attaquants :** Utilisation de "commits imposteurs" camouflés en correctifs de sécurité légitimes. La nature interconnectée des dépôts (forks) permet à ces commits malveillants d'être référencés comme des SHA valides.
*   **Insuffisance des solutions actuelles :** Bien que les *workflow lockfiles* introduits par GitHub permettent de lier les exécutions à des commits spécifiques et d'écarter certains forks, ils ne garantissent pas la sécurité intrinsèque des dépendances, ne résolvent pas les problèmes de builds dynamiques (Docker) et ne sont pas disponibles sur GitHub Enterprise Server.

**Vulnérabilités identifiées :**
*   **Exploitation des Forks :** Possibilité d'injecter du code via des forks qui partagent des références avec le dépôt upstream.
*   **Builds Runtime :** Les actions basées sur Docker peuvent compiler leurs images à l'exécution, important des dépendances non verrouillées malgré un SHA fixe.
*   **Absence de vérification d'auteur :** Le pinning ne vérifie pas la signature ou la légitimité de l'auteur du commit.

**Recommandations :**
*   **Ne pas considérer le SHA pinning comme une solution finale :** Il s'agit d'une mesure nécessaire mais largement insuffisante.
*   **Adopter des catalogues d'actions approuvées :** Utiliser des ensembles d'actions rigoureusement vérifiés et centralisés au sein de l'organisation.
*   **Surveillance accrue de la chaîne CI/CD :** Appliquer des politiques de sécurité plus strictes qui vont au-delà du simple verrouillage de versions, incluant l'audit des dépendances transitives et la validation de la provenance du code.
*   **Révision des pipelines :** Auditer les actions qui effectuent des builds dynamiques au moment de l'exécution pour s'assurer de la stabilité et de la sécurité des composants importés.

---
[Source](https://thehackernews.com/2026/11/hackers-found-way-around-github-sha.html){:target="_blank"}
