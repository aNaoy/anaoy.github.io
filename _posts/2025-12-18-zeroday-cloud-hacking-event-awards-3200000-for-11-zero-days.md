---
title: 'Zeroday Cloud hacking event awards $320,0000 for 11 zero days'
date: 2025-12-18
permalink: /posts/2025/12/18/zeroday-cloud-hacking-event-awards-3200000-for-11-zero-days/
tags:
- veille-cyber
- bleepingcomp
---
**Récompenses pour les Vulnérabilités Critiques dans l'Infrastructure Cloud**

Une compétition de cybersécurité axée sur le cloud a récompensé des chercheurs à hauteur de 320 000 dollars pour la découverte et la démonstration de 11 vulnérabilités critiques "zero-day" (inconnues jusqu'alors). Ces failles, exploitées avec succès dans 85% des tentatives, concernaient des composants essentiels utilisés dans les environnements cloud, notamment des bases de données populaires comme Redis, PostgreSQL et MariaDB, ainsi que le noyau Linux.

**Points Clés :**

*   **Montant des récompenses :** 320 000 $ décernés pour 11 vulnérabilités zero-day.
*   **Participants :** Wiz Research, en partenariat avec Amazon Web Services, Microsoft et Google Cloud.
*   **Taux de succès :** 85% des tentatives d'exploitation réussies lors de 13 sessions de piratage.
*   **Principales technologies ciblées :** Redis, PostgreSQL, Grafana, MariaDB et le noyau Linux.
*   **Catégories sans exploits identifiés :** IA (Ollama, vLLM, Nvidia Container Toolkit), Kubernetes, Docker, serveurs web (nginx, Apache Tomcat, Envoy, Caddy), Apache Airflow, Jenkins, et GitLab CE.

**Vulnérabilités Identifiées (avec CVE si disponibles) :**

*   **Redis :** Vulnérabilités permettant l'exécution de code à distance.
*   **PostgreSQL :** Vulnérabilités permettant l'exécution de code à distance.
*   **Grafana :** Vulnérabilités permettant l'exécution de code à distance.
*   **MariaDB :** Vulnérabilités permettant l'exécution de code à distance.
*   **Noyau Linux :** Une faille d'évasion de conteneur (container escape) permettant de briser l'isolation entre les locataires du cloud.

*(Note : Les identifiants CVE spécifiques pour ces vulnérabilités n'ont pas été mentionnés dans l'article.)*

**Recommandations :**

Bien que l'article ne détaille pas de recommandations spécifiques post-découverte, les résultats soulignent l'importance de :

*   **Veille de sécurité proactive :** Identifier et corriger rapidement les vulnérabilités zero-day dans les composants critiques du cloud.
*   **Renforcement de la sécurité des bases de données :** S'assurer que les configurations et les accès aux bases de données comme Redis, PostgreSQL et MariaDB sont sécurisés.
*   **Sécurité du noyau Linux :** Maintenir le noyau à jour et surveiller les tentatives d'évasion de conteneurs, une menace critique pour la sécurité multi-locataire.
*   **Protection des modèles d'IA :** La tentative échouée de cibler vLLM et Ollama met en évidence le potentiel risque pour les modèles d'IA, les jeux de données et les prompts privés.

---
[Source](https://www.bleepingcomputer.com/news/security/zeroday-cloud-hacking-event-awards-320-0000-for-11-zero-days/){:target="_blank"}
