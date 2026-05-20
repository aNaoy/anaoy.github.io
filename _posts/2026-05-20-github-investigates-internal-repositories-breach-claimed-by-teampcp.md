---
title: 'GitHub investigates internal repositories breach claimed by TeamPCP'
date: 2026-05-20
permalink: /posts/2026/05/20/github-investigates-internal-repositories-breach-claimed-by-teampcp/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission des dépôts internes de GitHub par TeamPCP

GitHub a confirmé l'accès non autorisé à environ 3 800 de ses dépôts internes suite à l'installation, par un employé, d'une extension Visual Studio Code (VS Code) malveillante. Le groupe de pirates TeamPCP revendique la possession de ces codes sources et tente de les vendre pour un montant minimum de 50 000 dollars, menaçant de publier les données gratuitement en l'absence d'acheteur. À ce jour, GitHub précise qu'aucune preuve n'indique une compromission des données des clients stockées en dehors de ses systèmes internes.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation d'une extension VS Code compromise sur le poste d'un collaborateur pour infiltrer l'infrastructure.
*   **Étendue :** Environ 3 800 dépôts internes sont concernés.
*   **Auteurs :** Le groupe TeamPCP, récidiviste dans les attaques de chaîne d'approvisionnement (précédemment impliqué dans des compromissions liées à Trivy, PyPI, NPM, Docker et des employés d'OpenAI).
*   **Statut :** Enquête interne en cours ; les clients seront notifiés si des impacts sur leurs propres données sont identifiés.

**Vulnérabilités :**
*   **Risque lié aux extensions d'environnement de développement (IDE) :** L'installation d'extensions tierces non vérifiées constitue une vulnérabilité critique permettant d'outrepasser les périmètres de sécurité. (Pas de CVE spécifique associée à cet incident, il s'agit d'une compromission de chaîne d'approvisionnement logicielle).

**Recommandations :**
*   **Gestion des extensions :** Restreindre strictement l'installation d'extensions dans les environnements de développement (VS Code, etc.) aux solutions approuvées et vérifiées par les équipes de sécurité.
*   **Zero Trust :** Appliquer les principes du moindre privilège aux postes de travail des développeurs pour limiter les accès latéraux en cas de compromission d'un terminal.
*   **Surveillance accrue :** Renforcer la supervision des logs d'accès aux infrastructures critiques et des activités de CI/CD.

---
[Source](https://www.bleepingcomputer.com/news/security/github-investigates-internal-repositories-breach-claimed-by-teampcp/){:target="_blank"}
