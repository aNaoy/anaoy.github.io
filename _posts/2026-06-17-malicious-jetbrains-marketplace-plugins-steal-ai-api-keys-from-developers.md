---
title: 'Malicious JetBrains Marketplace plugins steal AI API keys from developers'
date: 2026-06-17
permalink: /posts/2026/06/17/malicious-jetbrains-marketplace-plugins-steal-ai-api-keys-from-developers/
tags:
- veille-cyber
- bleepingcomp
---
### Vol massif de clés API IA via des plugins JetBrains Marketplace

Une campagne malveillante a été identifiée sur le JetBrains Marketplace, touchant au moins 15 plugins d'assistance au développement (IA, revue de code, utilitaires Git). Ces extensions, installées près de 70 000 fois, sont conçues pour exfiltrer les clés API des services d'IA (OpenAI, DeepSeek, SiliconFlow) renseignées par les utilisateurs.

**Points clés :**
* **Mécanisme d'exfiltration :** Dès que l'utilisateur enregistre sa clé API dans les paramètres, le plugin l'envoie en clair via une requête HTTP vers un serveur distant (`39.107.60[.]51`).
* **Modèle économique douteux :** Les attaquants proposent des versions payantes ("donations") au sein des plugins. En échange, le serveur renvoie une clé API fonctionnelle, probablement issue des identifiants volés aux utilisateurs gratuits, permettant aux attaquants de recycler les accès dérobés.
* **Persistance :** Bien que découverts, de nombreux plugins (dont *DeepSeek AI Assist* et *CodeGPT AI Assistant*) sont restés disponibles au téléchargement sur le Marketplace malgré leur dangerosité avérée.

**Vulnérabilités :**
* Aucune CVE n'est associée à cet incident, car il s'agit d'une campagne de malwares intégrée volontairement au code source des plugins (backdoor logicielle) plutôt qu'une exploitation de faille technique.

**Recommandations :**
* **Audit immédiat :** Vérifiez vos plugins installés sur votre IDE JetBrains et supprimez immédiatement tout outil suspect, en particulier ceux listés dans l'article (ex: *DeepSeek Junit Test*, *AI Git Commitor*, *CodeGPT AI Assistant*, etc.).
* **Révocation des secrets :** Si vous avez utilisé l'un de ces plugins, considérez que vos clés API sont compromises. Révoquez-les immédiatement sur les consoles de vos fournisseurs (OpenAI, DeepSeek, etc.) et générez-en de nouvelles.
* **Prudence lors de l'installation :** Limitez l'utilisation de plugins provenant de comptes inconnus ou récemment créés sur les places de marché. Privilégiez les extensions vérifiées et largement reconnues par la communauté.

---
[Source](https://www.bleepingcomputer.com/news/security/malicious-jetbrains-marketplace-plugins-steal-ai-api-keys-from-developers/){:target="_blank"}
