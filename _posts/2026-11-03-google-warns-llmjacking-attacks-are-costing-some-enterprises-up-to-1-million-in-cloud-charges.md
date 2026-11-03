---
title: 'Google Warns LLMjacking Attacks Are Costing Some Enterprises Up to $1 Million in Cloud Charges'
date: 2026-11-03
permalink: /posts/2026/11/03/google-warns-llmjacking-attacks-are-costing-some-enterprises-up-to-1-million-in-cloud-charges/
tags:
- veille-cyber
- hackernews
---
### L'essor du "LLMjacking" : le vol de ressources IA coûte des millions aux entreprises

Le "LLMjacking" est une forme de cybercriminalité émergente où des attaquants détournent les clés d'API et les accès aux modèles de langage (LLM) d'entreprises pour utiliser leurs ressources de calcul à des fins frauduleuses. Contrairement au minage de cryptomonnaies, cette pratique génère des coûts de facturation cloud massifs en quelques heures, dépassant parfois un million de dollars par victime.

**Points clés :**
* **Mécanisme :** Les attaquants ciblent les terminaux LLM exposés ou volent des jetons d'accès via du phishing, des dépôts GitHub publics ou des secrets mal configurés.
* **Monétisation :** Une nouvelle catégorie d'acteurs, les "LLM Mixers", agrège ces accès volés pour les revendre à bas prix sur des places de marché souterraines (ex: Jet Night), permettant à des tiers d'utiliser les quotas d'entreprises légitimes.
* **Impact :** Les secteurs visés sont variés (finance, industrie, technologie, pharmacie) avec des abus incluant le provisionnement de GPU, le streaming de modèles automatisés et l'hébergement de charges de travail malveillantes.

**Vulnérabilités identifiées :**
* **CVE-2026-40217 :** Vulnérabilité dans le logiciel de routage LiteLLM permettant une escalade de privilèges et l'exécution de code à distance.
* **Configuration insécurisée :** Utilisation de clés de comptes de service (Service Account keys) avec des permissions excessives et présence de secrets en clair dans les dépôts de code.
* **Détournement de CLI :** Reconfiguration malveillante des outils de ligne de commande (OpenAI Codex, Claude Code) pour acheminer les requêtes via des serveurs tiers.

**Recommandations :**
* **Gestion des secrets :** Éviter impérativement le stockage de clés d'API ou de jetons (GitHub PAT, IAM tokens) dans les dépôts de code ou les environnements non sécurisés.
* **Contrôle des accès :** Appliquer le principe du moindre privilège aux comptes de service et auditer régulièrement les permissions IAM pour détecter des créations de comptes non autorisées.
* **Surveillance proactive :** Mettre en place des alertes sur les pics de consommation de ressources cloud et surveiller les logs d'accès pour identifier des comportements de routage inhabituels.
* **Sécurisation des outils :** Veiller à l'intégrité des configurations des outils de développement (CLI) et éviter l'exécution de scripts provenant de sources non fiables censés modifier les paramètres de sandbox des modèles.

---
[Source](https://thehackernews.com/2026/11/google-warns-llmjacking-attacks-are.html){:target="_blank"}
