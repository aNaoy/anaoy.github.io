---
title: 'Australia arrests alleged TeamPCP hackers behind supply-chain attacks'
date: 2026-08-27
permalink: /posts/2026/08/27/australia-arrests-alleged-teampcp-hackers-behind-supply-chain-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Démantèlement du groupe de pirates TeamPCP en Australie

Deux hommes, âgés de 21 et 23 ans, ont été arrêtés en Australie pour leur implication dans le collectif de hackers **TeamPCP**. Ce groupe est responsable d'une vaste campagne d'attaques sur la chaîne d'approvisionnement logicielle (*supply chain attacks*) ayant touché plus d'un millier d'organisations à travers le monde.

**Points clés :**
* **Mode opératoire :** Injection de code malveillant dans des logiciels open-source populaires. Les développeurs intégraient involontairement ces composants compromis dans leurs propres applications, facilitant ainsi l'accès aux réseaux gouvernementaux, académiques et privés.
* **Impact :** Le groupe a permis le vol d'environ 500 000 identifiants et l'exfiltration de plus de 300 Go de données sensibles. Les coûts de remédiation à l'échelle mondiale se chiffrent en centaines de millions de dollars.
* **Cibles notables :** GitHub, OpenAI, Mistral AI, SAP, Trivy, LiteLLM et la Commission européenne.
* **Nature du groupe :** TeamPCP est décrit comme un collectif décentralisé d'acteurs se coordonnant via des forums spécialisés, Discord et Telegram.

**Vulnérabilités :**
Bien que les CVE spécifiques ne soient pas mentionnées, les attaques reposaient systématiquement sur la **compromission de paquets tiers** (via npm, PyPI, etc.) et l'exploitation de **GitHub Actions** pour injecter des malwares (infostealers) dans les flux de développement logiciel.

**Recommandations :**
* **Audit des dépendances :** Vérifier rigoureusement l'intégrité et la provenance des paquets open-source tiers avant intégration.
* **Sécurisation des secrets :** Ne jamais stocker de clés d'authentification ou de secrets dans le code source (utilisez des gestionnaires de secrets).
* **Surveillance du cycle de développement :** Implémenter des contrôles de sécurité dans les pipelines CI/CD pour détecter des comportements anormaux lors de l'exécution des scripts de build.
* **Authentification multi-facteurs (MFA) :** Renforcer l'accès aux plateformes de développement pour limiter l'impact en cas de vol d'identifiants.

---
[Source](https://www.bleepingcomputer.com/news/security/australia-arrests-alleged-teampcp-hackers-behind-supply-chain-attacks/){:target="_blank"}
