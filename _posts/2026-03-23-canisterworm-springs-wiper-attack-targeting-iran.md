---
title: '‘CanisterWorm’ Springs Wiper Attack Targeting Iran'
date: 2026-03-23
permalink: /posts/2026/03/23/canisterworm-springs-wiper-attack-targeting-iran/
tags:
- veille-cyber
- krebs
---
### CanisterWorm : Le groupe TeamPCP cible l'infrastructure cloud iranienne

Le groupe cybercriminel **TeamPCP** a déployé un ver malveillant, baptisé « **CanisterWorm** », visant spécifiquement les systèmes situés en Iran ou utilisant la langue farsi. Ce groupe, principalement motivé par l'extorsion financière, exploite des infrastructures cloud (Azure et AWS) en automatisant l'usage de vulnérabilités connues et de mauvaises configurations plutôt que de développer des exploits originaux.

**Points clés :**
*   **Infrastructure résiliente :** Le groupe utilise des « canisters » (contrats intelligents basés sur la blockchain ICP) pour héberger son infrastructure, rendant le démantèlement par les autorités extrêmement difficile.
*   **Attaques de la chaîne d'approvisionnement :** TeamPCP a compromis les outils de scan de vulnérabilités **Trivy** (Aqua Security) et **KICS** (Checkmarx) via leurs GitHub Actions pour diffuser des logiciels malveillants de vol de données.
*   **Comportement destructeur :** Le ver détecte la configuration système de la cible. S'il identifie une localisation en Iran, il déclenche un « wiper » (effaceur de données) sur les nœuds Kubernetes et les machines locales.
*   **Mode opératoire :** Le groupe s'empare de clés SSH, de jetons Kubernetes, de données d'identification cloud et de portefeuilles de cryptomonnaies.

**Vulnérabilités exploitées :**
*   **React2Shell :** Vulnérabilité exploitée pour infiltrer les serveurs.
*   **Mauvaises configurations :** APIs Docker exposées, clusters Kubernetes mal sécurisés et serveurs Redis.
*   **GitHub Actions :** Détournement de workflows CI/CD pour injecter du code malveillant dans des versions officielles de logiciels.

**Recommandations :**
*   **Sécuriser le cloud :** Auditer strictement les APIs exposées et les configurations des clusters Kubernetes. Ne jamais laisser de services comme Docker ou Redis accessibles sans authentification forte.
*   **Surveillance de la supply chain :** Vérifier l'intégrité des outils open-source utilisés dans les pipelines de déploiement (CI/CD) et limiter les permissions accordées aux GitHub Actions.
*   **Gestion des accès :** Révoquer et renouveler immédiatement les clés SSH, les jetons d'authentification cloud et les secrets de déploiement si des outils de sécurité compromis ont été utilisés dans l'environnement.
*   **Monitoring :** Surveiller les accès réseau suspects et les activités inhabituelles sur les nœuds Kubernetes en se concentrant sur les comportements de suppression de données.

---
[Source](https://krebsonsecurity.com/2026/03/canisterworm-springs-wiper-attack-targeting-iran/){:target="_blank"}
