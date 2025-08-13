---
title: 'Hackers leak Allianz Life data stolen in Salesforce attacks'
date: 2025-08-13
permalink: /posts/2025/08/13/hackers-leak-allianz-life-data-stolen-in-salesforce-attacks/
tags:
- veille-cyber
- bleepingcomp
---
**Fuite de Données chez Allianz Life suite à des Attaques Ciblant Salesforce**

Des données sensibles relatives à des partenaires commerciaux et à 2,8 millions de clients de l'assureur américain Allianz Life ont été divulguées. Ces informations proviennent d'une campagne d'attaques visant la plateforme Salesforce.

L'incident a été révélé par le groupe de pirates informatiques ShinyHunters, qui a revendiqué le vol et la diffusion des bases de données "Accounts" et "Contacts" d'Allianz Life. Ces ensembles de données contiennent des informations personnelles telles que les noms, adresses, numéros de téléphone, dates de naissance et numéros d'identification fiscale, ainsi que des données professionnelles comme les licences et les affiliations.

Les attaques contre Salesforce impliquent généralement des techniques d'ingénierie sociale pour convaincre les employés de lier des applications malveillantes à leurs instances Salesforce. Une fois cette connexion établie, les attaquants peuvent télécharger et exfiltrer des bases de données, qu'ils utilisent ensuite pour des demandes d'extorsion.

ShinyHunters affirme collaborer avec le groupe Scattered Spider pour ces opérations, avec des liens potentiels vers Lapsus$, un groupe connu pour de nombreuses cyberattaques par le passé.

**Points Clés :**

*   **Victime :** Allianz Life (2,8 millions d'enregistrements de données divulgués)
*   **Plateforme Ciblée :** Salesforce
*   **Acteurs de la Menace :** ShinyHunters, avec des revendications de liens avec Scattered Spider et Lapsus$.
*   **Type de Données :** Informations personnelles et professionnelles sensibles.
*   **Méthode d'Attaque :** Ingénierie sociale pour le vol de données via des applications OAuth malveillantes.

**Vulnérabilités :**

*   L'article ne mentionne pas de CVE spécifiques liées à cette attaque. La vulnérabilité réside dans la possibilité pour les acteurs malveillants d'exploiter l'authentification via OAuth pour accéder aux données.

**Recommandations :**

*   **Renforcer les contrôles d'accès :** Examiner et limiter les autorisations accordées aux applications tierces connectées à Salesforce.
*   **Sensibilisation des employés :** Former les employés aux risques de l'ingénierie sociale et à l'importance de ne pas autoriser des applications suspectes.
*   **Surveillance continue :** Mettre en place une surveillance proactive des activités sur les instances Salesforce pour détecter toute anomalie.
*   **Gestion des identités et des accès :** Assurer une gestion rigoureuse des identités et des accès pour minimiser la surface d'attaque.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-leak-allianz-life-data-stolen-in-salesforce-attacks/){:target="_blank"}
