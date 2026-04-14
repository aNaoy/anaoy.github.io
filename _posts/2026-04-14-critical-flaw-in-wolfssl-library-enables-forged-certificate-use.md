---
title: 'Critical flaw in wolfSSL library enables forged certificate use'
date: 2026-04-14
permalink: /posts/2026/04/14/critical-flaw-in-wolfssl-library-enables-forged-certificate-use/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique dans la bibliothèque wolfSSL

Une faille de sécurité majeure a été identifiée dans la bibliothèque TLS/SSL **wolfSSL**, largement utilisée dans les systèmes embarqués, l'IoT et les infrastructures critiques (plus de 5 milliards d'appareils concernés). Cette vulnérabilité permet à un attaquant de contourner la validation des certificats en exploitant une vérification défaillante des algorithmes de signature numérique.

**Points clés :**
*   **Nature du problème :** La bibliothèque omet de vérifier correctement la taille ou le type d'algorithme de hachage lors de la vérification des signatures cryptographiques (ECDSA, ECC, DSA, ML-DSA, Ed25519 et Ed448).
*   **Conséquences :** Un attaquant peut présenter un certificat forgé utilisant un condensat (digest) anormalement faible. Le système victime accepte alors une signature falsifiée, permettant à l'attaquant d'usurper l'identité d'un serveur ou d'établir une connexion malveillante légitime aux yeux de l'application.

**Vulnérabilité identifiée :**
*   **CVE-2026-5194 :** Défaut de validation cryptographique affectant la robustesse des signatures.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer la version **wolfSSL 5.9.1** (publiée le 8 avril), qui corrige cette faille.
*   **Vérification des dépendances :** Pour les systèmes utilisant wolfSSL via des paquets de distribution Linux ou des firmwares tiers, consulter les avis de sécurité spécifiques des fournisseurs (certains produits, comme MariaDB, n'étant pas affectés car n'utilisant pas wolfSSL pour leurs opérations cryptographiques).
*   **Audit de déploiement :** Évaluer les infrastructures critiques pour identifier les versions vulnérables et prioriser la mise à jour des dispositifs exposés.

---
[Source](https://www.bleepingcomputer.com/news/security/critical-flaw-in-wolfssl-library-enables-forged-certificate-use/){:target="_blank"}
