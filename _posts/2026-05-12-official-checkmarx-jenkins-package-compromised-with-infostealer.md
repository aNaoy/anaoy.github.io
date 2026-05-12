---
title: 'Official CheckMarx Jenkins package compromised with infostealer'
date: 2026-05-12
permalink: /posts/2026/05/12/official-checkmarx-jenkins-package-compromised-with-infostealer/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de la chaîne d'approvisionnement : Le plugin Jenkins de Checkmarx détourné

Le groupe de hackers « TeamPCP » a compromis le plugin Jenkins AST de Checkmarx en publiant une version malveillante (2026.5.09) sur la place de marché officielle. Cette attaque s'inscrit dans une série d'intrusions visant l'infrastructure de développement de Checkmarx, facilitées par la réutilisation de secrets et d'identifiants dérobés lors d'une attaque précédente contre le scanner Trivy.

**Points clés :**
* **Vecteur d'attaque :** Accès non autorisé aux dépôts GitHub de Checkmarx via des identifiants compromis.
* **Impact :** Injection de code malveillant dans le plugin Jenkins, permettant le vol d'informations d'identification sur les environnements des développeurs.
* **Historique :** Checkmarx a subi plusieurs incidents de sécurité depuis mars, incluant des fuites de données GitHub revendiquées par le groupe LAPSUS$.
* **Détection :** La version malveillante ne respectait pas le format de numérotation officiel et ne possédait ni tag Git ni publication GitHub associée.

**Vulnérabilités :**
* Aucune CVE spécifique n'est attribuée, car l'attaque repose sur une compromission de la chaîne d'approvisionnement logicielle via l'utilisation détournée d'identifiants de compte à privilèges.

**Recommandations :**
* **Vérification de version :** S'assurer impérativement d'utiliser la version officielle **2.0.13-829.vc72453fa_1c16** (ou versions antérieures légitimes) et supprimer toute version suspecte.
* **Réinitialisation des accès :** En cas d'utilisation de la version compromise, considérer tous les secrets (clés API, mots de passe, tokens) comme compromis et procéder à une rotation immédiate.
* **Audit de sécurité :** Rechercher des traces de mouvement latéral ou de persistance au sein des serveurs Jenkins et des environnements CI/CD.
* **Hygiène de sécurité :** Appliquer une politique stricte de rotation des secrets pour prévenir l'exploitation d'identifiants volés.

---
[Source](https://www.bleepingcomputer.com/news/security/official-checkmarx-jenkins-package-compromised-with-infostealer/){:target="_blank"}
