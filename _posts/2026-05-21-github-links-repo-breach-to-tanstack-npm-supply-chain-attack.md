---
title: 'GitHub links repo breach to TanStack npm supply-chain attack'
date: 2026-05-21
permalink: /posts/2026/05/21/github-links-repo-breach-to-tanstack-npm-supply-chain-attack/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de GitHub via une extension VS Code malveillante

GitHub a été victime d'une intrusion ayant touché environ 3 800 de ses dépôts internes. L'incident a été causé par l'installation, par un employé, d'une version malveillante de l'extension VS Code **Nx Console** (version 18.95.0), infectée dans le cadre de la campagne d'attaque par chaîne d'approvisionnement visant **TanStack**. Attribuée au groupe **TeamPCP**, cette attaque a permis aux assaillants de voler des identifiants et des secrets (AWS, Kubernetes, npm, etc.) via le poste de travail compromis.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation d'une extension de développement légitime détournée pour exfiltrer des identifiants (notamment via le GitHub CLI).
*   **Impact :** Accès non autorisé à des dépôts privés ; le groupe TeamPCP tente actuellement de vendre ces données pour 50 000 $.
*   **Réponse :** GitHub a sécurisé le périphérique compromis et procédé à une rotation massive des secrets critiques.
*   **Persistance :** L'extension malveillante a été disponible brièvement sur le marketplace VS Code et OpenVSX, touchant un nombre restreint d'utilisateurs directs, mais avec des conséquences importantes sur la chaîne d'approvisionnement logicielle.

**Vulnérabilités :**
*   **GHSA-c9j4-9m59-847w :** Vulnérabilité spécifique à la version 18.95.0 de l'extension Nx Console.

**Recommandations :**
*   **Vigilance sur les extensions :** Limiter l'installation d'extensions VS Code aux outils vérifiés et audités.
*   **Gestion des secrets :** Rotation immédiate des clés d'accès (AWS, GCP, GitHub tokens) en cas de compromission suspectée d'un poste de développeur.
*   **Surveillance CI/CD :** Renforcer la surveillance des flux de travail automatisés pour détecter toute activité inhabituelle ou non autorisée provenant de comptes compromis.
*   **Politique "Zero Trust" :** Réduire les privilèges accordés aux comptes de développeurs et isoler les environnements de développement des infrastructures de production critiques.

---
[Source](https://www.bleepingcomputer.com/news/security/github-links-repo-breach-to-tanstack-npm-supply-chain-attack/){:target="_blank"}
