---
title: 'Windows 10 OOB update released to fix Message Queuing (MSMQ) issues'
date: 2025-12-19
permalink: /posts/2025/12/19/windows-10-oob-update-released-to-fix-message-queuing-msmq-issues/
tags:
- veille-cyber
- bleepingcomp
---
**Mise à Jour de Sécurité pour Windows 10 Corrige les Problèmes de Message Queuing**

Une mise à jour de sécurité étendue pour Windows 10, publiée le 9 décembre 2025, a entraîné des dysfonctionnements du service Message Queuing (MSMQ), un composant essentiel pour la gestion des tâches en arrière-plan dans les environnements d'entreprise. Microsoft a rapidement publié une mise à jour hors bande (OOB), KB5074976, disponible uniquement via le catalogue de mises à jour de Microsoft, pour résoudre ces problèmes.

**Points Clés :**

*   La mise à jour de sécurité de décembre 2025 a involontairement affecté la fonctionnalité MSMQ de Windows 10.
*   Les symptômes incluent des files d'attente de messages inactives, des erreurs de ressources insuffisantes, des échecs d'écriture dans les files d'attente, et des messages d'erreur liés à la création de messages ou à l'espace disque/mémoire.
*   Le problème touche principalement les environnements d'entreprise et gérés, y compris les configurations MSMQ en cluster sous charge.
*   Les éditions Windows Home ou Pro sur des appareils personnels sont peu susceptibles d'être affectées.
*   La mise à jour hors bande (KB5074976) doit être téléchargée manuellement depuis le catalogue de mises à jour de Microsoft et s'adresse spécifiquement aux systèmes éligibles aux mises à jour de sécurité étendues (ESU) et rencontrant ces problèmes.

**Vulnérabilités :**

Aucune CVE spécifique n'est mentionnée dans l'article, mais le problème réside dans une mauvaise configuration ou une interaction inattendue introduite par une mise à jour de sécurité dans le fonctionnement de MSMQ.

**Recommandations :**

*   Les entreprises utilisant Windows 10 et ayant installé la mise à jour de décembre 2025 doivent vérifier le bon fonctionnement de MSMQ.
*   Si des problèmes sont constatés, il est impératif de télécharger et d'installer la mise à jour hors bande KB5074976 depuis le catalogue de mises à jour de Microsoft.
*   Les utilisateurs d'appareils personnels sous Windows 10 Home ou Pro ne devraient pas être concernés.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/windows-10-oob-update-released-to-fix-message-queuing-msmq-issues/){:target="_blank"}
