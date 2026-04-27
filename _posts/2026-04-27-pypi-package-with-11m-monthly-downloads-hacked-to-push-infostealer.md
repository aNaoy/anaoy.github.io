---
title: 'PyPI package with 1.1M monthly downloads hacked to push infostealer'
date: 2026-04-27
permalink: /posts/2026/04/27/pypi-package-with-11m-monthly-downloads-hacked-to-push-infostealer/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de la supply chain : le package PyPI « elementary-data » détourné

Le package open-source *elementary-data*, largement utilisé pour l'observabilité des données (plus de 1,1 million de téléchargements mensuels), a été victime d'une attaque par injection de script compromettant sa version 0.23.3. Contrairement à un piratage de compte de mainteneur classique, l'attaquant a exploité une vulnérabilité dans le workflow d'intégration continue (GitHub Actions) pour injecter du code malveillant directement dans le processus de build officiel.

**Points clés :**
*   **Mode opératoire :** L'attaquant a utilisé une injection de script via un commentaire malveillant sur une *pull request*, permettant d'exécuter du code arbitraire lors du workflow.
*   **Escalade :** L'attaque a permis de dérober le `GITHUB_TOKEN` du workflow, facilitant la création d'un commit et d'un tag signés, et déclenchant la publication automatique du package corrompu sur PyPI et du conteneur infecté sur GitHub Container Registry.
*   **Impact :** La charge utile (contenue dans `elementary.pth`) visait le vol massif de données sensibles (clés SSH, identifiants cloud, jetons CI, portefeuilles de cryptomonnaies, historique shell et fichiers de configuration).

**Vulnérabilités :**
*   Injection de commande dans les workflows GitHub Actions (non identifiée par une CVE spécifique dans l'article, mais liée à une mauvaise gestion des entrées utilisateur dans les pipelines CI/CD).

**Recommandations :**
*   **Mise à jour immédiate :** Passer à la version 0.23.4 (ou supérieure) qui corrige la faille.
*   **Rotation des secrets :** Toute machine ayant téléchargé la version 0.23.3 (ou les images Docker taguées `0.23.3` et `latest`) doit être considérée comme compromise. Il est impératif de réinitialiser tous les secrets (AWS, GCP, Azure, clés SSH, tokens API, etc.).
*   **Sécurisation :** Restaurer les environnements affectés à partir d'une sauvegarde saine.
*   **Bonnes pratiques :** Utiliser des versions de dépendances « épinglées » (pinned versions) dans vos fichiers de configuration pour éviter l'installation automatique de versions malveillantes lors de mises à jour silencieuses.

---
[Source](https://www.bleepingcomputer.com/news/security/pypi-package-with-11m-monthly-downloads-hacked-to-push-infostealer/){:target="_blank"}
