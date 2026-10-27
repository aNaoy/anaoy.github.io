---
title: 'OpenAI Compaction Flaw Let Researchers Bypass Hidden Reasoning Protections'
date: 2026-10-27
permalink: /posts/2026/10/27/openai-compaction-flaw-let-researchers-bypass-hidden-reasoning-protections/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité de l'API OpenAI : Le contournement des traces de raisonnement via la "Compaction"

Des chercheurs en cybersécurité ont identifié une faille dans la fonctionnalité de "compaction" d'OpenAI, permettant d'extraire en texte clair les traces de raisonnement normalement chiffrées des modèles d'IA (tels que `gpt-5.6-sol`).

**Points clés :**
*   **Mécanisme de l'attaque :** La fonction de compaction, conçue pour condenser les conversations, traite les données en interne. En manipulant les instructions données au processus de compaction (notamment en demandant une copie fidèle avec remplacement des espaces par des tabulations pour contourner les filtres), les attaquants pouvaient forcer l'inclusion des traces de raisonnement dans l'objet compacté.
*   **Contournement des protections :** Cette méthode a contourné les sécurités mises en place en août contre le "replay" entre différents modèles, car la compaction est effectuée par le modèle lui-même, évitant ainsi les contrôles de sécurité inter-modèles.
*   **Intérêt de l'extraction :** L'accès à ces traces permet la distillation de modèles (l'entraînement de modèles moins coûteux sur les données de modèles propriétaires), ce qui constitue un avantage concurrentiel majeur et une menace pour la propriété intellectuelle.

**Vulnérabilités :**
*   Aucune CVE n'a été attribuée, car il s'agit d'une vulnérabilité logique au sein du service API d'OpenAI (corrigée côté serveur par l'éditeur).

**Recommandations :**
*   **Pour les développeurs :** Aucune action n'est requise. Le correctif a été déployé par OpenAI le 23 octobre.
*   **Pour OpenAI :** Les chercheurs soulignent que des correctifs isolés ne suffisent pas. Toute étape côté serveur capable de lire du raisonnement déchiffré tout en suivant des instructions utilisateur présente un risque de fuite de données et nécessite une refonte de l'isolation des processus de traitement.

---
[Source](https://thehackernews.com/2026/10/openai-compaction-flaw-let-researchers.html){:target="_blank"}
