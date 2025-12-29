---
title: '27 Malicious npm Packages Used as Phishing Infrastructure to Steal Login Credentials'
date: 2025-12-29
permalink: /posts/2025/12/29/27-malicious-npm-packages-used-as-phishing-infrastructure-to-steal-login-credentials/
tags:
- veille-cyber
- hackernews
---
## Exploitation de Packages npm pour le Phishing et le Vol d'Identifiants

Une campagne sophistiquée a utilisé 27 packages malveillants sur le registre npm pour héberger des pages de phishing visant à dérober des identifiants de connexion. Ces packages étaient destinés à du personnel commercial et de vente dans des organisations liées aux infrastructures critiques aux États-Unis et dans les nations alliées. L'objectif n'était pas l'installation directe des packages, mais l'exploitation de npm et des CDNs de livraison de contenu comme infrastructure d'hébergement résiliente.

Les pages de phishing créées imitent des portails de partage de documents et des pages de connexion Microsoft, avec l'adresse e-mail souvent pré-remplie. Ces techniques visent à tromper les victimes en leur faisant croire qu'elles interagissent avec des services légitimes. Les packages incluaient diverses mesures anti-analyse, comme le filtrage de bots, l'évasion de sandboxes et l'utilisation de champs de formulaire cachés pour piéger les robots d'exploration. Le code JavaScript était également obfuscé pour compliquer l'inspection automatisée.

L'infrastructure utilisée dans cette campagne présente des similitudes avec celle associée à Evilginx, un kit de phishing open-source, suggérant un lien potentiel avec des activités d'attaques par l'homme du milieu (AitM). Les packages contenaient 25 adresses e-mail codées en dur, appartenant à des individus travaillant dans des secteurs tels que la fabrication, l'automatisation industrielle, la plasturgie et la santé, dans divers pays. La méthode d'obtention de ces adresses est inconnue, mais une collecte d'informations publiques lors de salons professionnels est suspectée.

Face à ce risque, il est recommandé de renforcer la vérification des dépendances, de surveiller les requêtes CDN inhabituelles, d'imposer une authentification multifacteur (MFA) résistante au phishing et de détecter les activités suspectes post-authentification. L'article mentionne également une augmentation des malwares destructeurs sur les registres de packages, qui ciblent spécifiquement les données importantes pour les développeurs.

**Points Clés :**

*   Utilisation de 27 packages npm malveillants comme infrastructure d'hébergement pour des pages de phishing.
*   Ciblage de personnels commerciaux dans des organisations d'infrastructures critiques.
*   Exploitation de npm et des CDNs comme infrastructure d'hébergement résiliente.
*   Techniques d'usurpation de sites de partage de documents et de pages de connexion Microsoft.
*   Mesures d'anti-analyse et d'évasion pour compliquer la détection.
*   Similitudes avec l'infrastructure d'Evilginx.
*   Codage en dur d'adresses e-mail spécifiques de personnes ciblées.

**Vulnérabilités / Vecteurs d'Attaque :**

*   Manque de vérification rigoureuse des packages sur les registres npm, permettant l'hébergement de code malveillant.
*   La confiance accordée aux dépendances de packages open-source sans analyse approfondie.
*   Les techniques de phishing toujours efficaces pour tromper les utilisateurs.

**Recommandations :**

*   Mettre en place une vérification stricte des dépendances de packages.
*   Journaliser et surveiller les requêtes CDN inhabituelles provenant de contextes non-développement.
*   Imposer une authentification multifacteur (MFA) résistante au phishing.
*   Surveiller les événements suspects après authentification.
*   Sensibiliser les utilisateurs aux techniques de phishing.

---
[Source](https://thehackernews.com/2025/12/27-malicious-npm-packages-used-as.html){:target="_blank"}
