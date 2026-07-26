---
title: 'GitHub, PyPI add time-absed defenses against supply chain attacks'
date: 2026-07-26
permalink: /posts/2026/07/26/github-pypi-add-time-absed-defenses-against-supply-chain-attacks/
tags:
- veille-cyber
- bleepingcomp
---
# Renforcement de la sécurité de la chaîne d'approvisionnement logicielle : GitHub et PyPI

GitHub et PyPI ont implémenté de nouvelles mesures basées sur des délais temporels pour contrer la prolifération de paquets malveillants au sein de leurs écosystèmes, une réponse directe à des campagnes récentes comme *s1ngularity*, *Shai-Hulud* et *GhostAction*.

### Points clés
* **Mécanisme de latence (Cooldown) sur Dependabot :** GitHub introduit un délai par défaut de 72 heures avant de proposer des mises à jour automatiques des dépendances. Cela permet aux outils de sécurité de détecter et signaler les paquets malveillants avant qu'ils ne soient intégrés par les développeurs.
* **Restriction de publication sur PyPI :** La plateforme bloque désormais l'ajout de nouveaux fichiers à une version existante après un délai de 14 jours suivant sa publication initiale.
* **Approche préventive :** Si PyPI n'a pas encore subi d'attaque confirmée par "empoisonnement de version", cette mesure vise à neutraliser de manière proactive les risques liés au vol de jetons de publication.

### Vulnérabilités ciblées
* **Empoisonnement de la chaîne d'approvisionnement (Supply Chain Poisoning) :** Injection de code malveillant dans des paquets légitimes ou création de nouveaux paquets frauduleux.
* **Compromission de jetons/flux de travail :** Utilisation de jetons volés pour modifier des releases anciennes et considérées comme "sûres".
* **Installation automatisée immédiate :** Adoption de nouveaux paquets compromis par les développeurs avant que la communauté ou les outils de sécurité n'aient le temps de réagir.
*(Aucune CVE spécifique n'est mentionnée dans l'article, ces mesures ciblant des vecteurs d'attaque généraux).*

### Recommandations pour les développeurs
* **Configuration personnalisée :** Ajuster le délai de *cooldown* de Dependabot selon les besoins spécifiques du projet.
* **Verrouillage des dépendances :** Utiliser systématiquement des fichiers de verrouillage (*lockfiles*) pour garantir l'intégrité des versions installées.
* **Gestion des accès :** Privilégier les jetons à portée restreinte (*restricted-scope tokens*).
* **Sécurisation de l'intégration continue (CI) :** Désactiver les scripts d'installation inutiles lors des processus de CI/CD pour limiter l'exécution de code arbitraire.

---
[Source](https://www.bleepingcomputer.com/news/security/github-pypi-add-time-absed-defenses-against-supply-chain-attacks/){:target="_blank"}
