---
title: 'Critical SolarWinds Serv-U flaws offer root access to servers'
date: 2026-02-24
permalink: /posts/2026/02/24/critical-solarwinds-serv-u-flaws-offer-root-access-to-servers/
tags:
- veille-cyber
- bleepingcomp
---
**Mises à jour critiques pour SolarWinds Serv-U : Risque d'accès administrateur**

Des vulnérabilités critiques ont été corrigées dans le logiciel de transfert de fichiers SolarWinds Serv-U, permettant potentiellement à des attaquants d'obtenir un accès administrateur ("root" ou "admin") sur les serveurs non corrigés.

**Points Clés :**

*   SolarWinds a publié des mises à jour de sécurité pour quatre vulnérabilités critiques dans Serv-U, qui pouvaient mener à l'exécution de code à distance.
*   La faille la plus grave, CVE-2025-40538, permet à des attaquants disposant de privilèges élevés d'obtenir des permissions d'administrateur système.
*   D'autres failles corrigées incluent deux problèmes de confusion de type et une vulnérabilité de référence directe d'objet non sécurisée (IDOR), pouvant également mener à l'exécution de code avec des privilèges élevés.
*   L'exploitation de ces failles nécessite que l'attaquant possède déjà des privilèges élevés sur le serveur ciblé.
*   Le logiciel Serv-U est une cible fréquente pour les cyberattaques, car il donne accès à des données potentiellement sensibles.

**Vulnérabilités :**

*   **CVE-2025-40538 :** Défaut de contrôle d'accès permettant à un attaquant de créer un utilisateur administrateur système et d'exécuter du code arbitraire en tant que "root" via des privilèges d'administrateur de domaine ou de groupe.
*   Deux vulnérabilités de confusion de type.
*   Une vulnérabilité de référence directe d'objet non sécurisée (IDOR).
*   *Historiquement, des failles précédentes comme CVE-2021-35211 et CVE-2024-28995 ont également été exploitées.*

**Recommandations :**

*   Appliquer immédiatement les mises à jour de sécurité fournies par SolarWinds pour Serv-U, notamment la version 15.5.4.

---
[Source](https://www.bleepingcomputer.com/news/security/critical-solarwinds-serv-u-flaws-offer-root-access-to-servers/){:target="_blank"}
