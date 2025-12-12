---
title: 'Brave browser starts testing agentic AI mode for automated tasks'
date: 2025-12-12
permalink: /posts/2025/12/12/brave-browser-starts-testing-agentic-ai-mode-for-automated-tasks/
tags:
- veille-cyber
- bleepingcomp
---
**Brave Innove avec une IA de Navigation Automatisée et Sécurisée**

Le navigateur Brave teste une nouvelle fonctionnalité baptisée "mode de navigation IA agentique", qui exploite son assistant IA, Leo, pour automatiser diverses tâches. Cette innovation permet des actions comme la recherche web autonome, la comparaison de produits, la recherche de codes promotionnels et le résumé d'actualités. Actuellement en phase de test sur la version Nightly de Brave, cette option est désactivée par défaut.

**Risques et Mesures de Sécurité**

Brave reconnaît les dangers inhérents à l'IA agentique, notamment les attaques par injection de prompt et le risque d'interprétation erronée des intentions de l'utilisateur. Pour contrer ces menaces, le mode IA fonctionne dans un profil isolé, sans accès aux cookies, aux informations de connexion ou aux données sensibles de l'utilisateur. Il est également restreint dans son accès à des zones critiques comme les paramètres du navigateur, les sites non-HTTPS et le Chrome Web Store. Toutes ses actions sont transparentes pour l'utilisateur, et les opérations risquées nécessitent une approbation explicite.

Un mécanisme de "vérification d'alignement" surveille les actions de l'IA, s'assurant qu'elles correspondent à l'intention de l'utilisateur, similaire à ce qui a été annoncé pour Gemini sur Chrome. Ce second modèle isolé est protégé contre les attaques par injection de prompt ciblant le modèle principal. Brave renforce sa protection en intégrant des règles basées sur des politiques et en utilisant des modèles entraînés pour atténuer les injections de prompt. La confidentialité des données reste une priorité, avec le maintien du blocage des publicités et des traqueurs, une politique de non-journalisation, et l'assurance que les données utilisateur ne seront pas utilisées pour l'entraînement des modèles IA.

**Accès et Tests**

Pour tester cette nouvelle fonctionnalité, il faut utiliser la version Brave Nightly et activer le drapeau "Brave’s AI browsing" dans `brave://flags`. Une fois activé, un bouton apparaîtra dans la boîte de dialogue de Leo pour lancer le mode IA. Brave encourage les retours des testeurs pour améliorer la fonction et a doublé ses primes de bug bounty pour les soumissions concernant cette IA de navigation.

---
[Source](https://www.bleepingcomputer.com/news/artificial-intelligence/brave-browser-starts-testing-agentic-ai-mode-for-automated-tasks/){:target="_blank"}
