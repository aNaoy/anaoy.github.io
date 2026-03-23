---
title: 'We Found Eight Attack Vectors Inside AWS Bedrock. Heres What Attackers Can Do with Them'
date: 2026-03-23
permalink: /posts/2026/03/23/we-found-eight-attack-vectors-inside-aws-bedrock-heres-what-attackers-can-do-with-them/
tags:
- veille-cyber
- hackernews
---
### Vecteurs d'attaque et risques de sécurité dans AWS Bedrock

AWS Bedrock, bien que puissant pour l'intégration de modèles d'IA aux données d'entreprise, présente une surface d'attaque étendue. La recherche menée par XM Cyber identifie huit vecteurs exploitant principalement des configurations permissives et des intégrations mal sécurisées, plutôt que des failles intrinsèques aux modèles d'IA.

**Points clés et vecteurs d'attaque :**

*   **Manipulation des logs (Model Invocation) :** Exfiltration de données sensibles via le détournement des logs vers des buckets S3 contrôlés par l'attaquant ou suppression des traces forensiques.
*   **Compromission des bases de connaissances (RAG) :** Accès direct aux sources de données (S3, Salesforce, SharePoint) ou aux bases de données vectorielles (Pinecone, Aurora) via le vol d'identifiants de connexion.
*   **Détournement d'agents :** Modification des instructions de base ou injection d'exécuteurs malveillants, permettant des actions non autorisées (modification de base de données, création d'utilisateurs).
*   **Attaques indirectes sur les agents :** Injection de code malveillant dans les fonctions Lambda ou les couches (layers) dont dépendent les agents pour leurs tâches.
*   **Manipulation des flux (Flows) :** Insertion de nœuds malveillants dans les workflows pour intercepter des données ou contourner les contrôles d'autorisation.
*   **Dégradation des Guardrails :** Affaiblissement ou suppression des filtres de sécurité, rendant le système vulnérable aux injections de prompts et aux contenus toxiques.
*   **Empoisonnement des prompts managés :** Modification centralisée des templates de prompts pour altérer le comportement des agents en temps réel, sans nécessiter de redéploiement applicatif.

**Vulnérabilités :**
Aucune CVE spécifique n'est mentionnée, l'article soulignant que ces menaces reposent sur une gestion inadéquate des permissions (IAM) et des privilèges excessifs accordés aux identités accédant aux ressources AWS.

**Recommandations de sécurité :**

*   **Principe du moindre privilège :** Auditer et restreindre strictement les permissions IAM liées à Bedrock (notamment les actions `Update`, `Create` et `Delete`).
*   **Gestion des identités :** Sécuriser les identifiants utilisés pour les intégrations SaaS et les bases de données afin d'éviter les mouvements latéraux.
*   **Surveillance et posture :** Cartographier précisément les chemins d'attaque potentiels traversant l'infrastructure cloud et les systèmes sur site.
*   **Contrôle des configurations :** Maintenir une surveillance rigoureuse sur les Guardrails et les templates de prompts pour détecter toute altération inopinée du comportement de l'IA.

---
[Source](https://thehackernews.com/2026/03/we-found-eight-attack-vectors-inside.html){:target="_blank"}
