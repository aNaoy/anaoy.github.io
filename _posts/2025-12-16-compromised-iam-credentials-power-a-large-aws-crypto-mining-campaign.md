---
title: 'Compromised IAM Credentials Power a Large AWS Crypto Mining Campaign'
date: 2025-12-16
permalink: /posts/2025/12/16/compromised-iam-credentials-power-a-large-aws-crypto-mining-campaign/
tags:
- veille-cyber
- hackernews
---
### Campagne de Minage de Cryptomonnaies sur AWS Exploitant des Identifiants IAM Compromis

Une campagne de minage de cryptomonnaies à grande échelle cible les utilisateurs d'Amazon Web Services (AWS) en exploitant des identifiants d'Identity and Access Management (IAM) compromis. Détectée en novembre 2025, cette menace utilise de nouvelles techniques de persistance pour compliquer la réponse aux incidents.

L'attaquant, opérant depuis un hébergeur externe, procède rapidement à la découverte des ressources et des permissions avant de déployer des mineurs de cryptomonnaies sur les services ECS et EC2. L'accès initial, obtenu via des identifiants IAM aux privilèges élevés, permet à l'attaquant de sonder l'environnement et de tester ses permissions sans coûts significatifs en utilisant l'API `RunInstances` avec le drapeau "DryRun". Cette étape vise à valider l'aptitude de l'infrastructure à accueillir le logiciel de minage.

Une fois les permissions vérifiées, l'attaquant utilise les API `CreateServiceLinkedRole` et `CreateRole` pour créer des rôles IAM destinés aux groupes d'autoscaling et à AWS Lambda, avant d'attacher la politique "AWSLambdaBasicExecutionRole" au rôle Lambda. La campagne a vu la création de dizaines de clusters ECS, parfois plus de 50 dans une seule attaque. Le rôle malveillant, hébergé sur DockerHub sous le nom "yenik65958/secret:user", est utilisé pour démarrer le minage de cryptomonnaies sur les nœuds ECS Fargate via l'algorithme RandomVIREL. De plus, des groupes d'autoscaling sont configurés pour un redimensionnement massif, visant à exploiter les quotas de service EC2 et maximiser la consommation de ressources.

Les instances ciblées incluent celles à haute performance GPU, d'apprentissage automatique, ainsi que des instances de calcul, de mémoire et d'usage général. Une technique de persistance notable consiste à utiliser l'action `ModifyInstanceAttribute` pour désactiver la terminaison des instances via API, empêchant ainsi leur suppression facile et prolongeant la durée des opérations de minage. Cette méthode a déjà été démontrée comme pouvant être exploitée pour la prise de contrôle d'instances et d'autres actions malveillantes. Par ailleurs, une fonction Lambda est créée et peut être invoquée par n'importe quel principal, couplée à un utilisateur IAM disposant d'une politique d'accès complet à Amazon SES, ouvrant la voie à des attaques de phishing.

**Points clés :**

*   Exploitation d'identifiants IAM compromis pour le minage de cryptomonnaies sur AWS.
*   Utilisation de techniques de persistance avancées, notamment la désactivation de la terminaison des instances via API.
*   Déploiement à grande échelle sur les services ECS et EC2.
*   Création de rôles IAM pour l'autoscaling et Lambda.
*   Utilisation d'une image Docker malveillante pour déployer le mineur RandomVIREL.
*   Création de groupes d'autoscaling massifs pour maximiser l'utilisation des ressources.
*   Potentiel d'utilisation d'Amazon SES pour des attaques de phishing.

**Vulnérabilités :**

*   **Compromission d'identifiants IAM :** L'absence de mesures de sécurité adéquates autour des identifiants IAM permet l'accès non autorisé.
*   **Permissions IAM trop larges :** Des privilèges excessifs accordés aux identifiants IAM facilitent la cascade d'actions malveillantes.
*   **Absence de mécanismes de détection et de réponse robustes :** Les techniques de persistance visent à contourner ou retarder les efforts de réponse.
*   **(Non spécifié par CVE dans l'article) :** L'abus de l'API `ModifyInstanceAttribute` avec le paramètre `disableApiTermination` est identifié comme un risque sécuritaire.

**Recommandations :**

*   Renforcer les contrôles d'identité et de gestion des accès.
*   Implémenter l'utilisation de credentials temporaires plutôt que des clés d'accès à long terme.
*   Utiliser l'authentification multifacteur (MFA) pour tous les utilisateurs.
*   Appliquer le principe du moindre privilège (PoLP) aux principaux IAM.
*   Ajouter des contrôles de sécurité des conteneurs pour scanner les images suspectes.
*   Surveiller les demandes inhabituelles d'allocation de CPU dans les définitions de tâches ECS.
*   Utiliser AWS CloudTrail pour enregistrer les événements sur les services AWS.
*   Assurer l'activation d'AWS GuardDuty pour faciliter les flux de réponse automatisés.

---
[Source](https://thehackernews.com/2025/12/compromised-iam-credentials-power-large.html){:target="_blank"}
