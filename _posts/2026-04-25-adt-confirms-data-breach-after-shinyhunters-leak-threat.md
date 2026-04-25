---
title: 'ADT confirms data breach after ShinyHunters leak threat'
date: 2026-04-25
permalink: /posts/2026/04/25/adt-confirms-data-breach-after-shinyhunters-leak-threat/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission des données chez ADT par le groupe ShinyHunters

La société de sécurité résidentielle ADT a confirmé une fuite de données personnelles suite à une intrusion survenue le 20 avril. Le groupe de cybercriminels ShinyHunters, qui revendique le vol de 10 millions d'enregistrements, menace de publier ces informations en l'absence de paiement d'une rançon.

**Points clés :**
* **Nature de l'intrusion :** Le groupe aurait utilisé une attaque par *vishing* (hameçonnage vocal) pour compromettre les identifiants d'un employé sur une plateforme SSO (Okta).
* **Vecteur d'accès :** Une fois le compte SSO compromis, les attaquants ont accédé à l'instance Salesforce de l'entreprise pour exfiltrer les données.
* **Données impactées :** Noms, numéros de téléphone et adresses. Pour une minorité de clients, les dates de naissance et les quatre derniers chiffres du numéro de sécurité sociale ou d'identification fiscale ont été consultés.
* **Ce qui est préservé :** Les systèmes de sécurité des clients sont intacts et aucune information bancaire ou de paiement n'a été dérobée.

**Vulnérabilités :**
* L'incident exploite une faille humaine (ingénierie sociale) plutôt qu'une vulnérabilité logicielle spécifique, rendant caducs les mécanismes de protection des comptes SSO (Okta) par le vol de session ou d'identifiants légitimes. Aucune CVE n'est associée à cet incident.

**Recommandations :**
* **Renforcement de l'authentification :** Implémenter l'authentification multi-facteurs (MFA) résistante au phishing, telle que l'utilisation de clés de sécurité matérielles (FIDO2/WebAuthn), pour neutraliser l'efficacité du *vishing*.
* **Sensibilisation :** Former les employés, en particulier ceux ayant des accès privilégiés aux applications SaaS, à la détection des tentatives d'ingénierie sociale par téléphone.
* **Gestion des accès :** Appliquer le principe du moindre privilège sur les applications critiques comme Salesforce et surveiller les accès inhabituels ou provenant de localisations géographiques suspectes sur les solutions SSO.

---
[Source](https://www.bleepingcomputer.com/news/security/adt-confirms-data-breach-after-shinyhunters-leak-threat/){:target="_blank"}
