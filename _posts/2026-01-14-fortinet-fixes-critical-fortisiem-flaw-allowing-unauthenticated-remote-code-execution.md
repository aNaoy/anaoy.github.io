---
title: 'Fortinet Fixes Critical FortiSIEM Flaw Allowing Unauthenticated Remote Code Execution'
date: 2026-01-14
permalink: /posts/2026/01/14/fortinet-fixes-critical-fortisiem-flaw-allowing-unauthenticated-remote-code-execution/
tags:
- veille-cyber
- hackernews
---
### Correction Critique de FortiSIEM : Exécution de Code à Distance Non Authentifiée

Une faille critique dans FortiSIEM, identifiée comme **CVE-2025-64155**, permet à un attaquant non authentifié d'exécuter du code à distance. Cette vulnérabilité de type injection de commande système (CWE-78), notée 9.4/10, affecte les nœuds Super et Worker.

**Points Clés :**

*   **Mécanisme :** La vulnérabilité réside dans la manière dont le service `phMonitor` de FortiSIEM, utilisé pour la surveillance de la santé et la communication inter-nœuds via le port TCP 7900, traite les requêtes relatives à la journalisation des événements de sécurité. Il permet une injection d'arguments via des requêtes TCP craftées.
*   **Impact :** L'exploitation permet initialement une écriture de fichier arbitraire en tant qu'utilisateur admin. Cette capacité peut être utilisée pour écrire un reverse shell dans un fichier exécuté périodiquement avec des privilèges root ( `/opt/charting/redishb.sh`), menant à une élévation de privilèges complète et à un contrôle total de l'appareil.
*   **Absence d'Authentification :** Le service `phMonitor` expose des gestionnaires de commandes qui ne nécessitent aucune authentification, facilitant l'exploitation par tout attaquant ayant un accès réseau au port 7900.

**Vulnérabilités Identifiées :**

*   **CVE-2025-64155 :** Injection de commande système (OS command injection) permettant l'exécution de code non autorisé.

**Versions Affectées et Recommandations :**

Fortinet a publié des correctifs pour les versions suivantes. Il est impératif de migrer ou de mettre à niveau vers les versions corrigées :

*   **FortiSIEM 6.7.0 à 6.7.10 :** Migrer vers une version corrigée.
*   **FortiSIEM 7.0.0 à 7.0.4 :** Migrer vers une version corrigée.
*   **FortiSIEM 7.1.0 à 7.1.8 :** Mettre à niveau vers la version 7.1.9 ou supérieure.
*   **FortiSIEM 7.2.0 à 7.2.6 :** Mettre à niveau vers la version 7.2.7 ou supérieure.
*   **FortiSIEM 7.3.0 à 7.3.4 :** Mettre à niveau vers la version 7.3.5 ou supérieure.
*   **FortiSIEM 7.4.0 :** Mettre à niveau vers la version 7.4.1 ou supérieure.
*   **FortiSIEM 7.5 et FortiSIEM Cloud :** Non affectés.

**Recommandations Supplémentaires :**

*   En attendant la mise à jour, Fortinet recommande de limiter l'accès au port `phMonitor` (7900).
*   Une autre vulnérabilité critique (CVE-2025-47855, CVSS 9.3) a été corrigée dans FortiFone, permettant à un attaquant non authentifié d'obtenir la configuration de l'appareil. Les versions affectées de FortiFone (3.0.13 à 3.0.23 et 7.0.0 à 7.0.1) doivent être mises à jour.

---
[Source](https://thehackernews.com/2026/01/fortinet-fixes-critical-fortisiem-flaw.html){:target="_blank"}
