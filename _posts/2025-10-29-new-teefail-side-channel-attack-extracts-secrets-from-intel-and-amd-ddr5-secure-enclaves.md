---
title: 'New TEE.Fail Side-Channel Attack Extracts Secrets from Intel and AMD DDR5 Secure Enclaves'
date: 2025-10-29
permalink: /posts/2025/10/29/new-teefail-side-channel-attack-extracts-secrets-from-intel-and-amd-ddr5-secure-enclaves/
tags:
- veille-cyber
- hackernews
---
**Une nouvelle attaque par canal auxiliaire sape la sécurité des environnements d'exécution de confiance (TEE)**

Une faille baptisée TEE.Fail, découverte par des chercheurs, permet d'extraire des informations sensibles des environnements d'exécution de confiance (TEE) des processeurs Intel et AMD, y compris ceux utilisant les technologies SGX, TDX, SEV-SNP et Ciphertext Hiding.

L'attaque repose sur un dispositif matériel peu coûteux, capable d'intercepter tout le trafic mémoire des serveurs équipés de mémoire DDR5. Elle permet d'accéder aux clés cryptographiques, y compris aux clés d'attestation, même sur des systèmes réputés sécurisés. Cette vulnérabilité peut être exploitée pour compromettre la confidentialité des machines virtuelles et simuler des attestations de conformité erronées. L'attaque affecte également le calcul confidentiel sur GPU Nvidia, permettant l'exécution de charges de travail non protégées sous couvert de sécurité.

Cette méthode se distingue des attaques précédentes par sa cible : la mémoire DDR5, la norme la plus récente, là où d'autres ciblaient la DDR4. L'encryption AES-XTS utilisée par Intel et AMD est jugée trop déterministe pour contrer ces attaques physiques d'interception de bus mémoire.

**Points clés :**

*   **Nature de l'attaque :** Canal auxiliaire par interposition matérielle sur le bus mémoire DDR5.
*   **Objectif :** Extraction de secrets et de clés cryptographiques des TEE.
*   **Technologies affectées :** Intel SGX, Intel TDX, AMD SEV-SNP, AMD Ciphertext Hiding.
*   **Coût de l'attaque :** Inférieur à 1000 USD grâce à du matériel standard.
*   **Conséquences :** Compromission de la confidentialité des données dans les machines virtuelles, falsification des attestations de sécurité, exploitation du calcul confidentiel GPU.

**Vulnérabilités :**

*   L'encryption AES-XTS est déterministe et insuffisante face aux attaques d'interception de bus mémoire.
*   Les implémentations actuelles d'Intel et AMD pour les TEE sur DDR5 ne préviennent pas ces attaques physiques.
*   Même avec des implémentations de code en temps constant comme OpenSSL et l'activation du Ciphertext Hiding, l'attaque TEE.Fail reste efficace.

**Recommandations :**

*   Les chercheurs suggèrent l'utilisation de contre-mesures logicielles pour atténuer les risques liés à l'encryption déterministe, bien que celles-ci soient coûteuses.
*   AMD et Intel considèrent ce type d'attaques physiques comme hors de leur champ d'application et n'ont pas prévu de correctifs pour le moment.

---
[Source](https://thehackernews.com/2025/10/new-teefail-side-channel-attack.html){:target="_blank"}
