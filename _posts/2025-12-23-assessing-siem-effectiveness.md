---
title: 'Assessing SIEM effectiveness'
date: 2025-12-23
permalink: /posts/2025/12/23/assessing-siem-effectiveness/
tags:
- veille-cyber
- securelist
---
**Optimiser l'Efficacité des Systèmes SIEM**

Les systèmes SIEM sont des outils de surveillance et de détection de menaces complexes dont l'efficacité repose fortement sur leur configuration et les sources de données connectées. L'évolution constante des infrastructures et des tactiques d'attaque rend nécessaire une mise à jour régulière de ces systèmes pour qu'ils restent pertinents. Une évaluation périodique permet d'identifier les lacunes et d'optimiser leur fonctionnement.

**Points Clés et Vulnérabilités :**

*   **Inventaire des Sources d'Événements Incomplet :** Fréquemment, l'inventaire des sources connectées n'est pas mis à jour avec les changements d'infrastructure, limitant la détection. Cela peut inclure la surveillance d'un seul type de système d'exploitation sur des infrastructures mixtes.
*   **Flux de Données Manquant :** Un pourcentage significatif de collecteurs configurés n'envoient pas d'événements, rendant inutiles les règles de détection associées et créant des angles morts dans la surveillance.
*   **Couverture Insuffisante des Sources :** Tous les systèmes d'un même type (ex. serveurs Windows) ne sont pas toujours surveillés, ce qui peut laisser passer des incidents sur des segments non monitorés.
*   **Conservation Excessive des Données Brutes :** L'option "Keep raw event" peut doubler la taille des données et surcharger la base de données, souvent laissée activée par inadvertance après des tests de normalisation.
*   **Problèmes de Normalisation :** Un flux d'événements non normalisé, partiellement normalisé, mal interprété par des analyseurs basiques, ou l'utilisation d'analyseurs obsolètes, compromet la logique de détection.
*   **Faible Couverture de la Logique de Détection :** Plus de la moitié des sources connectées ne sont pas couvertes par des règles de corrélation, bien qu'elles consomment des ressources système.
*   **Alertes Excessives :** Une logique de détection générant un volume anormal d'alertes rend le traitement impossible, qu'il s'agisse de faux positifs ou de modifications de l'environnement.
*   **Absence d'Intégration des Indicateurs de Compromission (IoCs) :** Le manque d'intégration avec des flux de renseignements sur les menaces (Threat Intelligence) limite la capacité du SIEM à vérifier les objets contre des bases de réputation ou des listes noires.
*   **Système SIEM Non Maintenu :** Le manque de mise à jour de la configuration du SIEM pour refléter l'évolution de l'infrastructure et des menaces rend le système obsolète.
*   **Autres Problèmes Courants :** Désynchronisation entre la capacité de licence et la charge réelle, gestion laxiste des droits utilisateurs, organisation chaotique des ressources personnalisées, utilisation de configurations standard sans adaptation, et désactivation des intégrations natives (LDAP, DNS, GeoIP).

**Recommandations :**

*   **Auditer Régulièrement l'Infrastructure :** Comparer systématiquement les sources connectées au SIEM avec l'inventaire réel de l'infrastructure. Établir des priorités de surveillance basées sur les risques (accès distant, services externes, périmètre, postes clients, outils de sécurité en haute priorité).
*   **Surveiller la Santé des Collecteurs et des Flux d'Événements :** Vérifier l'état des collecteurs et analyser les statistiques d'événements reçus pour identifier les défaillances.
*   **Vérifier la Couverture des Sources :** Utiliser des requêtes pour identifier le nombre de sources uniques envoyant des logs d'un type donné et comparer ce chiffre au nombre réel de sources.
*   **Examiner les Configurations de Normalisation :** S'assurer que les analyseurs sont à jour, utilisés correctement, et envisager des mécanismes pour identifier les événements non normalisés.
*   **Développer et Maintenir la Logique de Détection :** Créer et documenter un registre des règles de détection, en s'assurant qu'elles couvrent les sources connectées.
*   **Optimiser les Règles de Détection :** Tester et affiner la logique de détection pour minimiser les faux positifs et réagir aux alertes excessives en analysant la cause racine.
*   **Intégrer les Indicateurs de Compromission :** Mettre en place et vérifier l'intégration des flux de Threat Intelligence, que ce soit via des intégrations natives, des systèmes de gestion de données de menace, ou des listes IoCs. Développer les règles de corrélation associées.
*   **Maintenir le SIEM à Jour :** Comparer la configuration actuelle avec la documentation initiale et adapter le système aux nouvelles infrastructures, menaces, et processus du SOC.
*   **Gérer les Ressources et les Intégrations :** S'assurer que la capacité de licence correspond à la charge, organiser les ressources personnalisées avec des conventions de nommage claires, adapter les configurations standard, et activer les intégrations natives.
*   **Structurer les Processus :** En général, améliorer l'efficacité du SIEM passe par la structuration des processus, la surveillance continue de la qualité à chaque étape (intégration des sources, développement des règles, normalisation), et des audits réguliers.

Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans l'article.

---
[Source](https://securelist.com/siem-effectiveness-assessment/118560/){:target="_blank"}
