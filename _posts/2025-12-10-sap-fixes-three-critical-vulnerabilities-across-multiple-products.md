---
title: 'SAP fixes three critical vulnerabilities across multiple products'
date: 2025-12-10
permalink: /posts/2025/12/10/sap-fixes-three-critical-vulnerabilities-across-multiple-products/
tags:
- veille-cyber
- bleepingcomp
---
**Mises à Jour Critiques de Sécurité SAP : Trois Vulnérabilités Majeures Corrigées**

SAP a récemment publié des correctifs pour 14 vulnérabilités identifiées dans divers produits, dont trois jugées critiques.

**Points Clés :**

*   **CVE-2025-42880 :** Une faille d'injection de code affectant SAP Solution Manager ST 720 (score CVSS : 9.9). Elle permet à un attaquant authentifié d'insérer du code malveillant via des appels de fonctions, potentiellement accordant un contrôle total du système. SAP Solution Manager est la plateforme de gestion de cycle de vie et de surveillance de SAP.
*   **CVE-2025-55754 :** Un ensemble de vulnérabilités Apache Tomcat impactant les composants SAP Commerce Cloud (versions HY\_COM 2205, COM\_CLOUD 2211, et COM\_CLOUD 2211-JDK21) (score CVSS : 9.6). SAP Commerce Cloud est une plateforme d'e-commerce pour les grandes enseignes.
*   **CVE-2025-42928 :** Une vulnérabilité de désérialisation touchant SAP jConnect (score CVSS : 9.1). Sous certaines conditions, elle pourrait permettre à un utilisateur privilégié d'exécuter du code à distance via des entrées spécialement conçues. SAP jConnect est un pilote JDBC pour connecter des applications Java à des bases de données SAP ASE et SAP SQL Anywhere.

Outre ces failles critiques, SAP a également résolu cinq vulnérabilités de haute gravité et six de gravité moyenne, incluant des problèmes de corruption de mémoire, des contrôles d'authentification et d'autorisation manquants, des attaques XSS, et des divulgations d'informations. Bien qu'aucune de ces 14 vulnérabilités n'ait été signalée comme activement exploitée, il est fortement recommandé de déployer les correctifs sans délai en raison de la criticité des systèmes SAP dans les environnements d'entreprise.

---
[Source](https://www.bleepingcomputer.com/news/security/sap-fixes-three-critical-vulnerabilities-across-multiple-products/){:target="_blank"}
