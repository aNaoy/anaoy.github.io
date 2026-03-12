---
title: 'Findings Gadgets Like it’s 2026'
date: 2026-03-12
permalink: /posts/2026/03/12/findings-gadgets-like-its-2026/
tags:
- veille-cyber
- zerodaysfans
---
### Automatisation de la découverte de gadgets de désérialisation Java par LLM

L'utilisation d'outils comme *ysoserial* est devenue complexe et peu efficace pour identifier de nouvelles chaînes de gadgets dans les environnements Java modernes. Cette recherche démontre qu'un agent LLM (Claude Code), couplé à une analyse statique (WALA, ASM) et des boucles de rétroaction dynamiques, permet d'automatiser et d'accélérer la découverte de vulnérabilités de désérialisation.

#### Points clés
*   **Méthodologie** : Création d'un graphe d'appels à partir du *classpath*, interrogé par un LLM via une API REST. L'agent génère des tests, exécute les chaînes, débugue les échecs et affine ses tentatives de manière autonome.
*   **Contournement de JPMS** : L'utilisation de bibliothèques "shaded" (copies relocalisées de bibliothèques comme Xalan au sein de JAR tiers) permet de contourner les restrictions du *Java Platform Module System* (JPMS) introduites depuis le JDK 9, rendant à nouveau exploitables les gadgets de type `TemplatesImpl`.
*   **Performance** : Découverte de 17 chaînes, dont 6 inédites, sur des serveurs d'applications modernes (WildFly, Payara).

#### Vulnérabilités identifiées
*   **CB1-Shaded-RCE** : Exécution de code à distance (RCE) sur **WildFly** via une copie *shaded* de Xalan contenue dans `jakarta.servlet.jsp.jstl`. Le gadget `TemplatesImpl` est rendu exploitable malgré les protections du JDK 21.
*   **PriorityQueue-AttributeComparator-JNDI** : Nouvelle chaîne d'injection JNDI découverte sur **Payara**, utilisant `AttributeComparator` comme déclencheur de `toString()`, une méthode alternative aux approches classiques bloquées dans les versions récentes du JDK.
*   **Variantes CC4** : Nouvelles chaînes utilisant `TreeBag` ou `DualTreeBidiMap` comme points d'entrée, permettant de contourner les protections sur `PriorityQueue` et l'absence de sérialisation sur `InvokerTransformer` dans les versions récentes de Commons Collections.

#### Recommandations
*   **Audit des dépendances** : Identifier la présence de bibliothèques "shaded" ou d'anciennes versions de bibliothèques (Xalan, Commons-Collections, BeanUtils) au sein des serveurs d'applications et des dépendances applicatives.
*   **Filtrage de la désérialisation** : Ne pas se reposer uniquement sur les protections natives du JDK. Implémenter des mécanismes de *Look-ahead Deserialization* (filtres sélectifs) pour rejeter les classes suspectes avant qu'elles ne soient instanciées.
*   **Durcissement (Hardening)** :
    *   Surveiller les logs pour détecter des tentatives de JNDI Lookup ou des accès suspects à des classes internes.
    *   Mettre à jour les serveurs d'applications et supprimer les composants inutilisés (ex: les bibliothèques JSTL non nécessaires).
    *   Privilégier, dans la mesure du possible, des formats de sérialisation plus sûrs que la sérialisation native Java (JSON, Protobuf, etc.).

---
[Source](https://www.atredis.com/blog/2026/3/12/findings-gadgets-like-its-2026){:target="_blank"}
