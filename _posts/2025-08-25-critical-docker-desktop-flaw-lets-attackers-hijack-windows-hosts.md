---
title: 'Critical Docker Desktop flaw lets attackers hijack Windows hosts'
date: 2025-08-25
permalink: /posts/2025/08/25/critical-docker-desktop-flaw-lets-attackers-hijack-windows-hosts/
tags:
- veille-cyber
- bleepingcomp
---
## Attaque sur Docker Desktop : Compromission du système hôte

Une faille critique, identifiée sous la référence CVE-2025-9074, a été découverte dans Docker Desktop pour Windows et macOS. Cette vulnérabilité, notée 9.3, permet à un attaquant d'exécuter un conteneur malveillant pour accéder au moteur Docker, contournant ainsi les protections d'isolation des conteneurs (ECI).

**Points clés :**

*   Un conteneur malveillant peut interagir avec le moteur Docker sans avoir besoin de monter la "Docker socket".
*   Cela ouvre la voie à un accès non autorisé aux fichiers du système hôte.
*   L'isolation des conteneurs (ECI) n'offre pas de protection contre cette faille.
*   La faille permet d'atteindre l'API du moteur Docker sans authentification depuis un conteneur.

**Vulnérabilité :**

*   **Type :** Server-Side Request Forgery (SSRF)
*   **CVE :** CVE-2025-9074
*   **Impact :** Compromission du système hôte, permettant potentiellement le vol de données ou l'exécution de commandes administratives.

**Conséquences spécifiques :**

*   **Sur Windows :** L'exploitation de la faille, via WSL2, permet à l'attaquant de monter l'intégralité du système de fichiers en tant qu'administrateur. Il peut lire des fichiers sensibles et modifier des DLL système pour obtenir des privilèges d'administrateur sur l'hôte. L'exploit peut être réalisé avec très peu de code (quelques lignes de Python).
*   **Sur macOS :** Bien que des mesures de sécurité du système d'exploitation limitent l'étendue de l'impact (demande de permission pour accéder aux répertoires utilisateurs), un attaquant conserve un contrôle total sur l'application Docker et ses conteneurs. Ceci peut permettre des modifications de configuration ou l'introduction de portes dérobées.

**Recommandations :**

*   La faille a été corrigée par Docker dans la version 4.44.3 de Docker Desktop. Il est impératif de mettre à jour vers cette version ou une version ultérieure pour se protéger contre cette menace.

---
[Source](https://www.bleepingcomputer.com/news/security/critical-docker-desktop-flaw-lets-attackers-hijack-windows-hosts/){:target="_blank"}
