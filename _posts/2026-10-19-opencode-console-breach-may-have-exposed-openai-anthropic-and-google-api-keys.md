---
title: 'OpenCode Console Breach May Have Exposed OpenAI, Anthropic, and Google API Keys'
date: 2026-10-19
permalink: /posts/2026/10/19/opencode-console-breach-may-have-exposed-openai-anthropic-and-google-api-keys/
tags:
- veille-cyber
- hackernews
---
### Compromission des clés API chez OpenCode : Risques pour les utilisateurs d'IA

Le 16 octobre, une intrusion dans un système obsolète d'OpenCode a potentiellement exposé les clés API tierces (OpenAI, Anthropic, Google) stockées par 1,4 % des utilisateurs de son service hébergé, « Console ». Ces identifiants, essentiels pour appeler les modèles d'IA, ont permis à des attaquants d'effectuer des requêtes frauduleuses, générant des coûts importants pour certains clients.

**Points clés :**
* **Portée :** Seul le service « Console » est impacté ; les applications de bureau et en ligne de commande, qui stockent les clés localement, ne sont pas concernées.
* **Méthode :** L'attaque serait liée à une campagne de « distillation » (extraction de données pour entraîner des modèles concurrents) utilisant des clés API dérobées.
* **Conséquences financières :** Les attaquants utilisent les clés pour exécuter des requêtes facturables sur les comptes des utilisateurs. La suppression des clés dans l'interface Console ne suffit pas à les révoquer chez le fournisseur.

**Vulnérabilités :**
* Aucune CVE n'a été spécifiquement attribuée à cet incident, celui-ci résultant d'une intrusion dans un système hérité (legacy) vulnérable.

**Recommandations de sécurité :**
* **Révocation immédiate :** Annulez les clés API compromises directement depuis les tableaux de bord d'OpenAI, Anthropic ou Google et générez-en de nouvelles.
* **Mise à jour des systèmes :** Remplacez les anciennes clés dans toutes les applications, scripts et environnements de développement.
* **Audit et surveillance :** Vérifiez l'historique de facturation et d'utilisation de vos comptes API depuis le 16 octobre pour identifier toute activité suspecte.
* **Principe du moindre privilège :** Appliquez des limites de dépenses (budgets) sur les comptes fournisseurs et attribuez une clé API unique par outil pour faciliter la traçabilité et limiter les impacts en cas de fuite.

---
[Source](https://thehackernews.com/2026/10/opencode-console-breach-may-have.html){:target="_blank"}
