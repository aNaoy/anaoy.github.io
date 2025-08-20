---
title: 'Azure SSRF with Workflow Designer Feature'
date: 2025-08-20
permalink: /posts/2025/08/20/azure-ssrf-with-workflow-designer-feature/
tags:
- veille-cyber
- zerodaysfans
---
## Accès non autorisé aux métadonnées Azure via la fonctionnalité de Workflow Designer

Une vulnérabilité de type Server-Side Request Forgery (SSRF) a été identifiée dans la fonctionnalité de conception de flux de travail (Workflow Designer) d'une application Azure. Cette faille permettait à un attaquant d'accéder au Service de Métadonnées d'Instance Azure (IMDS), potentiellement pour récupérer des jetons d'accès.

**Points clés :**

*   La vulnérabilité exploitait une fonctionnalité permettant de configurer des appels à des API externes via des modèles de flux de travail.
*   En configurant un appel vers `http://169.254.169.254/metadata/instance?api-version=2020-06-01` avec l'en-tête `Metadata: true`, il était possible de récupérer des informations sur l'instance Azure.
*   La faille a permis de récupérer un jeton d'accès Azure avec des permissions de rôle "Contributor" (Contributeur).
*   La possibilité d'utiliser des expressions JPath sur la réponse de l'API externe a permis d'extraire le jeton d'accès complet.
*   La présence d'un mécanisme d'auto-enregistrement pour l'application a rendu cette vulnérabilité critique, car elle ouvrait la porte à une exploitation par de nombreux utilisateurs non autorisés.

**Vulnérabilité(s) :**

*   Server-Side Request Forgery (SSRF) dans la fonctionnalité de conception de flux de travail.

**Recommandations :**

*   Valider et assainir toutes les entrées utilisateur utilisées dans la configuration des appels d'API externes.
*   Restreindre l'accès aux services de métadonnées d'instance Azure uniquement aux processus autorisés et aux configurations de confiance.
*   Mettre en œuvre des contrôles d'accès stricts pour empêcher l'exploitation de fonctionnalités sensibles par des utilisateurs non authentifiés ou non autorisés.
*   Auditer régulièrement les applications pour détecter les vulnérabilités potentielles d'accès aux métadonnées.

---
[Source](https://blog.stratumsecurity.com/2025/08/20/azure-ssrf-with-workflow-designer-feature/){:target="_blank"}
