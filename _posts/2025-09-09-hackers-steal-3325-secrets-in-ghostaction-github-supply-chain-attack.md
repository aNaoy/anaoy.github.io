---
title: 'Hackers steal 3,325 secrets in GhostAction GitHub supply chain attack'
date: 2025-09-09
permalink: /posts/2025/09/09/hackers-steal-3325-secrets-in-ghostaction-github-supply-chain-attack/
tags:
- veille-cyber
- bleepingcomp
---
**Campagne GhostAction : Vol de Secrets via Chaîne d'Approvisionnement GitHub**

Une nouvelle attaque de la chaîne d'approvisionnement, baptisée "GhostAction", a ciblé GitHub, entraînant la compromission de 3 325 secrets. Ces informations volées incluent des clés et tokens pour des plateformes telles que PyPI, npm, DockerHub, ainsi que des tokens GitHub, Cloudflare et des identifiants AWS.

Détectée par les chercheurs de GitGuardian, l'attaque exploitait des comptes de mainteneurs compromis pour injecter des commits ajoutant des workflows GitHub Actions malveillants. Ces workflows se déclenchaient automatiquement lors de la publication de code ("push") ou manuellement. Une fois activés, ils lisaient les secrets de l'environnement Actions du projet et les transmettaient à un domaine externe contrôlé par les attaquants via une requête POST.

L'enquête a révélé que l'attaque était étendue, impactant au moins 817 dépôts, tous envoyant des données sensibles vers le même point d'exfiltration. Les attaquants ont identifié et exploité les noms des secrets légitimes pour les intégrer dans leurs propres workflows afin de voler divers types d'informations sensibles.

Bien que le projet FastUUID ait été l'un des premiers cas identifiés avec le vol de son token PyPI, aucune publication de package malveillant n'a eu lieu sur cet index avant la découverte et la remédiation.

**Points Clés :**

*   **Nature de l'attaque :** Chaîne d'approvisionnement logicielle sur GitHub.
*   **Mécanisme :** Injection de workflows GitHub Actions malveillants via des commits de comptes mainteneurs compromis.
*   **Action malveillante :** Lecture et exfiltration de secrets depuis l'environnement GitHub Actions vers un serveur externe.
*   **Portée :** 3 325 secrets volés, touchant au moins 817 dépôts.
*   **Impact sur les écosystèmes :** Atteinte à plusieurs écosystèmes de gestion de paquets (npm, PyPI, Rust crates) et potentiellement à des portefeuilles SDK entiers d'entreprises.

**Vulnérabilités :**

Aucune vulnérabilité spécifique (type CVE) n'est explicitement mentionnée dans l'article, mais l'attaque exploite la confiance accordée aux commits des mainteneurs légitimes et l'exposition des secrets configurés dans les workflows GitHub Actions.

**Recommandations :**

*   Surveiller activement les dépôts pour détecter des commits suspects ou des ajouts de workflows inconnus.
*   Révoquer immédiatement les tokens et clés compromis exposés dans les workflows GitHub Actions.
*   Mettre en place des contrôles d'accès stricts et une authentification forte pour les comptes des mainteneurs de dépôts.
*   Utiliser des outils de détection de secrets pour identifier et supprimer les informations sensibles intégrées dans le code ou les configurations.
*   Les équipes de sécurité des plateformes d'hébergement de code et des gestionnaires de paquets doivent renforcer leurs mécanismes de surveillance pour détecter ce type d'attaques.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-steal-3-325-secrets-in-ghostaction-github-supply-chain-attack/){:target="_blank"}
