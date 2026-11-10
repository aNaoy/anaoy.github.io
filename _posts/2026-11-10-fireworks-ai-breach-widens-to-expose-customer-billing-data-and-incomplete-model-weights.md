---
title: 'Fireworks AI Breach Widens to Expose Customer Billing Data and Incomplete Model Weights'
date: 2026-11-10
permalink: /posts/2026/11/10/fireworks-ai-breach-widens-to-expose-customer-billing-data-and-incomplete-model-weights/
tags:
- veille-cyber
- hackernews
---
### Expansion de la brèche chez Fireworks AI : Données clients et modèles exposés

L'entreprise Fireworks AI a confirmé que l'incident de sécurité survenu en octobre 2026 est plus étendu qu'initialement estimé. Après une intrusion initiale via des identifiants internes compromis, les attaquants ont accédé à l'environnement de développement de l'entreprise via un fournisseur cloud tiers, élargissant considérablement le périmètre des données exposées.

**Points clés :**
*   **Nature de l'attaque :** Il s'agit d'une campagne de « LLMjacking », où des cybercriminels détournent des infrastructures IA pour revendre l'accès à des modèles de langage à des tiers malveillants, tout en laissant les coûts à la charge des victimes.
*   **Données compromises :** Métadonnées de ressources, informations de facturation (adresses, historique des paiements), ainsi qu'un sous-ensemble de poids de modèles incomplets et des jeux de données.
*   **Impact tiers :** Notion, l'un des clients de Fireworks AI, a confirmé que moins de 1 % de ses espaces de travail ont été affectés, incluant potentiellement des transcriptions de chats utilisés pour sa fonctionnalité "Insights".
*   **Vulnérabilités :** Aucune CVE spécifique n'est associée à cet incident, l'attaque reposant sur le vol d'identifiants et l'exploitation de l'environnement de développement par un tiers.

**Recommandations :**
*   **Rotation immédiate :** Les clients dont les données ont été impactées doivent impérativement révoquer et renouveler leurs clés API, mots de passe et tout secret ayant pu être manipulé pendant la fenêtre d'intrusion.
*   **Renforcement de la sécurité :** Fireworks AI a procédé à une isolation des systèmes affectés, une révocation générale des identifiants compromis et un durcissement des contrôles d'accès.
*   **Surveillance :** Les entreprises utilisant des services d'infrastructure IA doivent améliorer leurs journaux d'audit et surveiller activement les activités inhabituelles sur leurs ressources cloud.

---
[Source](https://thehackernews.com/2026/11/fireworks-ai-breach-widens-to-expose.html){:target="_blank"}
