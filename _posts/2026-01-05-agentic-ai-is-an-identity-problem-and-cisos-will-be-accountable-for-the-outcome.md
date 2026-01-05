---
title: 'Agentic AI Is an Identity Problem and CISOs Will Be Accountable for the Outcome'
date: 2026-01-05
permalink: /posts/2026/01/05/agentic-ai-is-an-identity-problem-and-cisos-will-be-accountable-for-the-outcome/
tags:
- veille-cyber
- bleepingcomp
---
### L'Identité : Clé de la Sécurité des Agents IA

L'essor des agents d'intelligence artificielle (IA) en entreprise pose un défi majeur de sécurité axé sur la gestion des identités. Ces agents, qui agissent avec une intention similaire à celle des humains mais à l'échelle des machines, brouillent les frontières traditionnelles de la sécurité informatique. Contrairement aux identités humaines centralisées et prévisibles, les agents IA sont souvent décentralisés, faciles à créer, et capables d'opérer de manière autonome sur de multiples systèmes.

Les responsables de la sécurité informatique (CISO) se retrouvent ainsi face à une complexité accrue, car l'identité reste la cause première de nombreuses violations de données. L'octroi de larges permissions aux agents pour faciliter leur déploiement, le manque d'examen et de désactivation de leurs accès, ainsi que leur persistance même après la fin des projets qui les ont créés, créent des vulnérabilités. Les acteurs malveillants peuvent cibler ces identités surprivilégiées et toujours actives comme des points d'entrée idéaux.

Les outils de gestion des identités et des accès (IAM/PAM) actuels, conçus pour les utilisateurs humains ou les charges de travail prévisibles, peinent à s'adapter à cette nouvelle réalité. S'appuyer uniquement sur les fournisseurs de plateformes IA pour résoudre ces problèmes de sécurité identitaire est également risqué.

La solution réside dans l'application d'une discipline de gestion du cycle de vie des identités, similaire à celle utilisée pour les employés. Chaque agent IA doit avoir un propriétaire clairement identifié, un objectif explicite et mesurable, des accès alignés sur ses fonctions réelles, et une visibilité continue sur ses activités. La révocation automatique des accès doit être assurée lorsque les agents deviennent inactifs ou que les projets associés se terminent.

Une approche clé est de considérer la sécurité des agents IA comme un problème de corrélation de données. Le risque réel d'un agent ne se limite pas à son périmètre, mais englobe les ressources auxquelles il peut accéder : rôles cloud, applications SaaS, données sensibles, et autres identités. La corrélation des signaux d'identité à travers différentes couches (plateformes d'IA, fournisseurs d'identité, infrastructures, applications, données) est essentielle pour permettre aux CISO de répondre aux questions critiques lors des audits, des revues et des réponses aux incidents.

L'adoption de l'IA ne doit pas être freinée, mais abordée avec confiance par une gestion rigoureuse des identités. Les organisations qui réussiront seront celles qui reconnaîtront que la sécurisation des agents IA est une prérogative fondamentale liée à la gestion des identités, leur permettant ainsi de déployer cette technologie de manière durable, agile et sécurisée.

**Points Clés :**

*   L'IA agentique représente un nouveau type d'identité, décentralisé et autonome.
*   La gestion des identités est au cœur du problème de sécurité de l'IA agentique, avec les CISO responsables des résultats.
*   Les vulnérabilités proviennent de l'octroi excessif de privilèges et du manque de gestion du cycle de vie des identités des agents.
*   Les outils IAM/PAM traditionnels sont inadaptés aux spécificités des agents IA.
*   La solution repose sur la gestion du cycle de vie des identités, la corrélation des données et une visibilité accrue.

**Vulnérabilités :**

*   **Sur-privilégiation des agents :** Les agents se voient souvent accorder des permissions trop larges par commodité.
*   **Manque de revue et de désactivation :** Les accès des agents ne sont pas systématiquement examinés ni révoqués lorsqu'ils ne sont plus nécessaires.
*   **Identités persistantes et orphelines :** Les agents continuent d'opérer bien après la fin de leur projet ou la disparition de leur créateur.
*   **Corrélation d'identité insuffisante :** Difficulté à suivre et comprendre ce à quoi un agent a accès à travers différents systèmes.

**Recommandations :**

*   **Gérer le cycle de vie des identités des agents :** Appliquer le même principe que pour les identités humaines, de la création à la révocation.
*   **Attribution claire de la propriété :** Chaque agent doit être associé à un propriétaire clair au sein de l'Identity Provider.
*   **Objectifs explicites et mesurables :** Définir précisément le rôle et les fonctions de chaque agent.
*   **Accès basé sur le besoin réel :** Aligner les permissions sur les fonctions effectives de l'agent, pas sur la simplicité de configuration.
*   **Visibilité continue des activités :** Surveiller l'usage des agents pour détecter les dérives de privilèges.
*   **Révocation automatique des accès :** Mettre en place des mécanismes pour désactiver les accès des agents inactifs ou obsolètes.
*   **Corréler les signaux d'identité :** Fusionner les informations d'identité provenant des plateformes IA, des Identity Providers, des infrastructures, des applications et des données pour une vision complète du risque.
*   **Mettre en place des "guardrails" :** Fournir des cadres et des outils qui forcent la clarté sur l'intention et la portée des agents dès leur création.

---
[Source](https://www.bleepingcomputer.com/news/security/agentic-ai-is-an-identity-problem-and-cisos-will-be-accountable-for-the-outcome/){:target="_blank"}
