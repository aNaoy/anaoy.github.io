---
title: 'FBI warns of UNC6040, UNC6395 hackers stealing Salesforce data'
date: 2025-09-15
permalink: /posts/2025/09/15/fbi-warns-of-unc6040-unc6395-hackers-stealing-salesforce-data/
tags:
- veille-cyber
- bleepingcomp
---
**Cyberattaques ciblées sur Salesforce : Vols de données et extorsion**

Deux groupes de cybercriminels, identifiés comme UNC6040 et UNC6395, ciblent activement les environnements Salesforce des entreprises afin de dérober des données sensibles et de procéder à des extorsions.

**Points Clés :**

*   **Méthodes d'accès variées :** Les groupes utilisent différentes techniques pour pénétrer les systèmes. UNC6040 a recours à l'ingénierie sociale et au vishing (hameçonnage vocal) pour inciter les employés à connecter de fausses applications OAuth Salesforce Data Loader. UNC6395 a exploité des identifiants et jetons OAuth volés de Salesloft Drift pour accéder aux instances Salesforce.
*   **Données ciblées :** Les attaques visent initialement les tables de base de données "Accounts" et "Contacts" pour voler des informations sur les clients. Ultérieurement, l'accent a été mis sur les informations de cas de support, révélant des secrets, des identifiants et des jetons d'authentification (clés AWS, mots de passe, jetons Snowflake) pouvant servir à des intrusions ultérieures dans d'autres environnements cloud.
*   **Impact significatif :** De nombreuses grandes entreprises, notamment dans les secteurs de la technologie, de la mode et des services financiers, ont été victimes de ces attaques.
*   **Attribution présumée :** Le groupe ShinyHunters et d'autres acteurs se faisant appeler "Scattered Lapsus$ Hunters" revendiquent la responsabilité de ces activités. Ces groupes semblent avoir des liens avec les collectifs Lapsus$, Scattered Spider et ShinyHunters.
*   **Annonce de retrait :** Ces acteurs ont annoncé leur intention de "passer sous le radar" et de cesser de discuter de leurs opérations. Ils auraient également prétendu avoir obtenu un accès au système de vérification d'antécédents E-Check du FBI et au système de requêtes des forces de l'ordre de Google.

**Vulnérabilités :**

Bien que des CVE spécifiques ne soient pas explicitement mentionnés dans l'article pour ces attaques, les vulnérabilités exploitées sont liées à :

*   La défaillance des utilisateurs à identifier et refuser les applications malveillantes connectées via OAuth.
*   La compromission de dépôts GitHub de partenaires (comme Salesloft), entraînant le vol d'identifiants et de jetons d'authentification.
*   L'exposition potentielle d'informations sensibles dans les cas de support Salesforce.

**Recommandations :**

*   **Vigilance accrue :** Renforcer la sensibilisation des employés aux techniques d'ingénierie sociale et de vishing.
*   **Surveillance des applications OAuth :** Examiner attentivement et autoriser uniquement les applications OAuth nécessaires et de confiance pour accéder aux environnements Salesforce.
*   **Gestion des identifiants :** Mettre en œuvre des pratiques robustes de gestion des identifiants et de secrets, y compris la rotation régulière des clés et des jetons.
*   **Sécurisation des dépôts de code :** Les fournisseurs de services doivent sécuriser rigoureusement leurs dépôts de code pour prévenir le vol d'identifiants et de jetons.
*   **Surveillance des journaux :** Surveiller activement les journaux d'accès et d'activité de Salesforce pour détecter toute activité suspecte.
*   **Mise à jour des indicateurs de compromission :** Utiliser les indicateurs de compromission (IOC) publiés par le FBI pour renforcer les défenses.

---
[Source](https://www.bleepingcomputer.com/news/security/fbi-warns-of-unc6040-unc6395-hackers-stealing-salesforce-data/){:target="_blank"}
