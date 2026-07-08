---
title: 'GitHub Verified Commits Can Be Rewritten Into New Hashes Without Breaking Signatures'
date: 2026-07-08
permalink: /posts/2026/07/08/github-verified-commits-can-be-rewritten-into-new-hashes-without-breaking-signatures/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité des empreintes Git : La malléabilité des signatures « Verified »

Une recherche récente met en lumière une faille conceptuelle dans la manière dont GitHub gère les signatures de commits Git. Bien que les fichiers contenus dans un commit restent inchangés, il est possible de modifier la signature numérique d'un commit sans invalider son statut « Verified », ce qui génère une nouvelle empreinte (hash) pour un contenu identique.

**Points clés :**
* **Malléabilité des signatures :** Le hash d'un commit inclut les octets de la signature. En manipulant ces derniers (via des techniques cryptographiques connues), un attaquant peut modifier le hash du commit tout en conservant une signature valide.
* **Conséquences :** Les systèmes de sécurité, les outils de déduplication ou les listes de blocage (blocklists) basés sur le hash du commit peuvent être contournés, car un attaquant peut republier le même contenu sous un hash inconnu mais toujours « Verified ».
* **Absence de normalisation :** GitHub ne normalise pas les signatures avant vérification, acceptant des variantes non canoniques d'ECDSA, des champs ignorés dans RSA/EdDSA ou des structures DER non standards pour S/MIME.
* **Portée limitée :** Ce n'est pas une collision de hash ni une possibilité d'injecter du code malveillant ; le code final reste identique. La faille concerne la confiance accordée au hash comme identifiant unique et immuable.

**Vulnérabilités :**
Il n'existe **pas de CVE** attribuée, car le problème réside dans l'implémentation côté serveur (forge) et non dans le protocole Git lui-même.

**Recommandations :**
* **Pour les forges (GitHub, etc.) :** C'est aux fournisseurs de services d'implémenter une normalisation stricte des signatures (canonicalisation) avant de calculer le hash ou d'accorder le badge « Verified ».
* **Pour les développeurs :** Continuer à épingler (pinning) les actions et dépendances via leur hash complet reste une bonne pratique, car le contenu des fichiers reste intègre. Cependant, il ne faut pas considérer le statut « Verified » comme une garantie absolue d'unicité de l'identifiant du commit.
* **Systèmes tiers :** Les outils utilisant les hashs de commits pour la provenance ou le filtrage doivent normaliser les données avant de valider l'identité du commit.

---
[Source](https://thehackernews.com/2026/07/github-verified-commits-can-be.html){:target="_blank"}
