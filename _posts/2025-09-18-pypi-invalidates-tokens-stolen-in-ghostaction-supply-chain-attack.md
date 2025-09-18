---
title: 'PyPI invalidates tokens stolen in GhostAction supply chain attack'
date: 2025-09-18
permalink: /posts/2025/09/18/pypi-invalidates-tokens-stolen-in-ghostaction-supply-chain-attack/
tags:
- veille-cyber
- bleepingcomp
---
**Sécurité des dépôts de packages Python : Le piratage GhostAction neutralisé**

Une campagne de piratage, baptisée GhostAction, a visé les dépôts de packages Python (PyPI) en volant des jetons d'authentification utilisés pour publier des logiciels. Ces jetons ont été exfiltrés via des workflows GitHub Actions malveillants. Bien que plus de 3 300 secrets aient été dérobés, incluant divers types de jetons (PyPI, npm, DockerHub, GitHub, Cloudflare, AWS, etc.), le groupe responsable n'a pas réussi à les exploiter sur PyPI pour publier des logiciels malveillants.

**Points clés :**

*   Des workflows GitHub Actions compromis ont ciblé des dépôts de packages sur plusieurs écosystèmes (Python, Rust, JavaScript, Go).
*   Des jetons d'authentification (PyPI, npm, etc.) et des identifiants sensibles ont été dérobés.
*   Les acteurs malveillants n'ont pas réussi à abuser des jetons volés sur PyPI pour la publication de code malveillant.
*   Les tokens PyPI affectés ont été invalidés par la Python Software Foundation.

**Vulnérabilités :**

*   **Exfiltration de secrets via GitHub Actions :** Des workflows mal configurés ont permis d'envoyer des jetons d'authentification stockés en tant que secrets GitHub vers des serveurs externes. Aucune CVE spécifique n'est mentionnée pour cette vulnérabilité, elle découle d'une mauvaise utilisation des fonctionnalités de CI/CD.

**Recommandations :**

*   **Utilisation des Trusted Publishers :** Remplacer les jetons de longue durée par des jetons "Trusted Publishers" à courte durée de vie, spécialement pour les workflows GitHub Actions.
*   **Surveillance de l'historique des comptes :** Les mainteneurs de packages sont encouragés à se connecter à leurs comptes PyPI et à examiner leur historique de sécurité pour détecter toute activité suspecte.
*   **Rotation des jetons :** Les équipes affectées ont déjà été incitées à renouveler leurs jetons PyPI et à sécuriser leurs comptes.

---
[Source](https://www.bleepingcomputer.com/news/security/pypi-invalidates-tokens-stolen-in-ghostaction-supply-chain-attack/){:target="_blank"}
