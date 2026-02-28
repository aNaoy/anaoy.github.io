---
title: 'Thousands of Public Google Cloud API Keys Exposed with Gemini Access After API Enablement'
date: 2026-02-28
permalink: /posts/2026/02/28/thousands-of-public-google-cloud-api-keys-exposed-with-gemini-access-after-api-enablement/
tags:
- veille-cyber
- hackernews
---
**Clés d'API Google Cloud Exposeés : Un Risque Accru avec Gemini**

Des recherches récentes ont révélé qu'environ 3 000 clés d'API Google Cloud, généralement utilisées à des fins de facturation, ont été trouvées exposées sur Internet. Ces clés, portant le préfixe "AIza", étaient intégrées dans du code côté client pour fournir des services Google standards tels que des cartes intégrées sur des sites web. Le problème majeur survient lorsque l'API Gemini est activée sur un projet Google Cloud. Les clés d'API existantes de ce projet, même celles exposées publiquement, acquièrent alors la capacité de s'authentifier aux points d'accès sensibles de Gemini sans notification préalable.

Cette situation permet à des attaquants, ayant scraping ces clés depuis des sites web, d'accéder à des données privées, des fichiers téléchargés, des données mises en cache, et surtout, d'utiliser l'API Gemini à l'insu des propriétaires, entraînant des coûts considérables. De plus, la création de nouvelles clés d'API dans Google Cloud peut par défaut être configurée comme "sans restriction", leur permettant d'accéder à toutes les API activées, y compris Gemini.

Bien que Google ait réagi à cette découverte, déclarant avoir mis en place des mesures pour détecter et bloquer les clés d'API suspectes, un cas signalé sur Reddit fait état d'une facture de plus de 82 000 $ en deux jours due à l'utilisation d'une clé d'API Google Cloud prétendument volée.

**Points Clés:**

*   Près de 3 000 clés d'API Google Cloud ("AIza") ont été trouvées exposées publiquement.
*   L'activation de l'API Gemini sur un projet Google Cloud confère à ces clés la capacité de s'authentifier à Gemini.
*   Les attaquants peuvent exploiter ces clés pour accéder à des données privées, du cache, et générer des coûts via l'API Gemini.
*   La configuration par défaut des nouvelles clés d'API peut être "sans restriction", augmentant le risque.

**Vulnérabilités:**

*   Pas de CVE spécifique identifié dans l'article, mais la vulnérabilité réside dans le fait que des clés d'API destinées à la facturation peuvent être utilisées pour l'authentification à des services sensibles comme Gemini après activation de celui-ci. Le mécanisme de "sans restriction" par défaut est également une préoccupation majeure.

**Recommandations:**

*   Examiner attentivement les API et services activés dans les projets Google Cloud.
*   Vérifier si des API liées à l'intelligence artificielle sont activées et publiquement accessibles (par exemple, dans le JavaScript côté client ou dans des dépôts publics).
*   Si des API sont activées et que leurs clés sont exposées, les clés doivent être immédiatement remplacées (rotation).
*   Commencer la rotation par les clés les plus anciennes, car elles sont les plus susceptibles d'avoir été déployées publiquement avant que la menace ne soit comprise.
*   La sécurité des API doit être un processus continu, incluant des tests et des analyses de vulnérabilités, en tenant compte de l'évolution des risques dynamiques liés à l'intégration de l'IA.

---
[Source](https://thehackernews.com/2026/02/thousands-of-public-google-cloud-api.html){:target="_blank"}
