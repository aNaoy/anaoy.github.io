---
title: 'Mandiant details how ShinyHunters abuse SSO to steal cloud data'
date: 2026-01-31
permalink: /posts/2026/01/31/mandiant-details-how-shinyhunters-abuse-sso-to-steal-cloud-data/
tags:
- veille-cyber
- bleepingcomp
---
### Le Vishing Exploite les SSO pour le Vol de Données Cloud

Des attaques ciblées menées par des groupes comme ShinyHunters exploitent le vol d'identifiants et de codes d'authentification multifacteur (MFA) pour accéder aux données cloud. Ces attaques reposent sur le voice phishing (vishing), où les attaquants se font passer pour le personnel informatique et incitent les employés à visiter des sites de phishing ressemblant à leurs portails d'entreprise. Ces sites utilisent des kits avancés permettant aux attaquants d'obtenir les identifiants et les codes MFA en temps réel pendant l'appel.

Une fois l'accès obtenu, les attaquants s'introduisent dans les tableaux de bord SSO (comme Okta, Microsoft Entra, Google), qui répertorient les applications SaaS auxquelles l'utilisateur a accès. Ces applications, y compris Salesforce, Microsoft 365, et Google Drive, deviennent alors des cibles pour l'exfiltration de données. Les attaquants peuvent utiliser des outils comme des scripts PowerShell pour télécharger des données, modifier les journaux d'audit, voire installer des extensions malveillantes pour supprimer des preuves, comme l'extension "ToogleBox Recall" dans Google Workspace pour effacer des e-mails incriminants.

Plusieurs acteurs de la menace, regroupés sous les identifiants UNC6661, UNC6671 et UNC6240 (ShinyHunters), sont impliqués dans ces campagnes, utilisant des domaines de phishing enregistrés sous des noms variés imitant les portails d'entreprise. Les demandes d'extorsion sont ensuite envoyées, souvent sous le nom de ShinyHunters.

**Points Clés :**

*   **Méthode d'Attaque Principale :** Vishing combiné à des sites de phishing de type "credential harvesting" ciblant les identifiants SSO et les codes MFA.
*   **Objectif :** Accéder aux données sensibles stockées dans diverses applications SaaS via un compte compromis.
*   **Acteurs de la Menace :** Principalement ShinyHunters (UNC6240), mais aussi d'autres groupes comme UNC6661 et UNC6671.
*   **Techniques Post-Compromission :** Utilisation de scripts pour l'exfiltration de données, effacement de traces (e-mails de modification MFA, journaux), et installation d'extensions malveillantes.

**Vulnérabilités Exploité :**

*   **Compromission des Identifiants SSO :** Le vol des informations d'identification du compte d'un employé.
*   **Détournement du MFA :** L'exploitation de la confiance dans les notifications MFA pour les valider frauduleusement.
*   **Manque de Surveillance des Activités SaaS :** L'incapacité à détecter rapidement les exfiltrations de données ou les modifications anormales des configurations d'applications cloud.

**Recommandations :**

*   **Durcissement des flux d'identité et des réinitialisations d'authentification.**
*   **Collecte de journaux ("logging") pertinents pour la détection d'activités suspectes.**
*   **Mise en place de détections ciblant les comportements post-vishing :**
    *   Compromission de comptes SSO suivie d'une exfiltration de données rapide depuis les plateformes SaaS.
    *   Utilisation de PowerShell avec des User-Agents spécifiques accédant à SharePoint ou OneDrive.
    *   Autorisations OAuth inattendues pour des extensions comme "ToogleBox Recall" dans Google Workspace.
    *   Suppression d'e-mails de notification de modification MFA.
*   **Sensibilisation des employés aux techniques de vishing et de phishing.**
*   **Utilisation de solutions de sécurité capables de détecter des activités anormales sur les plateformes cloud et SSO.**

---
[Source](https://www.bleepingcomputer.com/news/security/mandiant-details-how-shinyhunters-abuse-sso-to-steal-cloud-data/){:target="_blank"}
