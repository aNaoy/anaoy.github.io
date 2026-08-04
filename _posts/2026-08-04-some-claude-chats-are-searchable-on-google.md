---
title: 'Some Claude Chats Are Searchable on Google'
date: 2026-08-04
permalink: /posts/2026/08/04/some-claude-chats-are-searchable-on-google/
tags:
- veille-cyber
- schneier
---
### Fuites de données confidentielles via les liens de partage Claude

De nombreuses conversations privées générées par l'IA Claude ont été indexées par les moteurs de recherche, exposant des informations sensibles telles que des clés de portefeuilles cryptographiques, des données médicales et des informations personnelles identifiables. Cette situation découle de la fonctionnalité de partage de liens d'Anthropic : lorsqu'un utilisateur génère un lien de partage, celui-ci devient publiquement accessible et peut être indexé par des outils tiers ou des moteurs de recherche.

**Points clés :**
*   **Responsabilité utilisateur :** Anthropic précise que les liens ne sont pas devinables. La fuite survient lorsque les utilisateurs partagent eux-mêmes ces liens, permettant leur indexation par des moteurs comme Google.
*   **Nature des données exposées :** Notes professionnelles, données de facturation médicale, clés privées de cryptomonnaies et adresses personnelles.
*   **Position d'Anthropic :** L'entreprise soutient que la confidentialité est maintenue par défaut et que le problème réside dans l'utilisation faite par les utilisateurs de la fonction de partage public.

**Vulnérabilités :**
*   Il ne s'agit pas d'une vulnérabilité technique (CVE) au sens classique du terme, mais d'un risque lié à la **gestion des permissions et au contrôle de l'accès aux données** (imprudence dans le partage de liens générés par l'application).

**Recommandations :**
*   **Audit des partages :** Vérifier et désactiver les liens de partage de conversations Claude via les paramètres de l'interface utilisateur.
*   **Prudence :** Ne jamais intégrer d'informations sensibles, confidentielles ou personnelles (PII) dans des outils d'IA basés sur le cloud.
*   **Politique de confidentialité :** Consulter la documentation officielle d'Anthropic concernant la gestion des conversations partagées pour s'assurer qu'aucun lien n'est actif sans nécessité absolue.

---
[Source](https://www.schneier.com/blog/archives/2026/08/some-claude-chats-are-searchable-on-google.html){:target="_blank"}
