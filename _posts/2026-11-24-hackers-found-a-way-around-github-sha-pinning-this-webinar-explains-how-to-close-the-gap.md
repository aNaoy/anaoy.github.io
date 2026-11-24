---
title: 'Hackers Found a Way Around GitHub SHA Pinning. This Webinar Explains How to Close the Gap'
date: 2026-11-24
permalink: /posts/2026/11/24/hackers-found-a-way-around-github-sha-pinning-this-webinar-explains-how-to-close-the-gap/
tags:
- veille-cyber
- hackernews
---
### Les limites de la sécurité par SHA pinning sur GitHub Actions

Le "SHA pinning" (fixer une version via son empreinte SHA) est devenu une mesure de sécurité standard pour protéger la chaîne d'approvisionnement logicielle. Cependant, des attaques récentes démontrent que cette pratique ne garantit pas la légitimité du code, mais uniquement son immuabilité. Les attaquants exploitent les mécanismes de "fork" de GitHub pour injecter du code malveillant qui semble provenir de dépôts officiels, contournant ainsi les politiques de sécurité des entreprises.

**Points clés :**
*   **Immuabilité ≠ Provenance :** Le SHA garantit que le code ne change pas, mais n'authentifie pas l'auteur ni la source réelle du commit.
*   **Vulnérabilité des forks :** GitHub permet aux forks de partager le même espace de noms/commits, facilitant l'insertion de commits malveillants masqués derrière des outils officiels (ex : cas de *Trivy* et *actions-cool*).
*   **Limites techniques :** Même avec le SHA, les actions basées sur Docker peuvent construire leur image à l'exécution, téléchargeant des dépendances non verrouillées.
*   **Limites des nouveaux "Lockfiles" :** Bien que les *workflow lockfiles* introduits par GitHub permettent de lier les exécutions à des commits spécifiques et d'atténuer le risque lié aux forks, ils ne garantissent pas la sécurité intrinsèque du code ni ne gèrent les builds dynamiques.

**Vulnérabilités :**
Aucune CVE spécifique n'est mentionnée, car il s'agit d'une vulnérabilité conceptuelle et structurelle liée à la confiance accordée au SHA sans vérification de la provenance (souvent appelée "impostor commits").

**Recommandations :**
*   **Ne pas considérer le pinning comme une finalité :** Il s'agit d'une défense nécessaire mais insuffisante.
*   **Vérification de la provenance :** S'assurer que les actions proviennent bien du dépôt amont (upstream) et non d'un fork non autorisé.
*   **Utilisation de catalogues sécurisés :** Privilégier l'usage d'un catalogue d'actions internes ou tierces préalablement auditées et approuvées.
*   **Surveillance accrue :** Ne pas se reposer uniquement sur les politiques automatiques de GitHub ; intégrer une revue des dépendances et du comportement des pipelines CI/CD.

---
[Source](https://thehackernews.com/2026/11/hackers-found-way-around-github-sha.html){:target="_blank"}
