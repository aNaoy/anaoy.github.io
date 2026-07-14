---
title: 'Microsoft Maps Three Salesforce Attack Paths Tied to a Year of ShinyHunters Activity'
date: 2026-07-14
permalink: /posts/2026/07/14/microsoft-maps-three-salesforce-attack-paths-tied-to-a-year-of-shinyhunters-activity/
tags:
- veille-cyber
- hackernews
---
### Menaces sur l'écosystème Salesforce : Abus de confiance et OAuth

Des acteurs malveillants, associés au groupe « ShinyHunters », exploitent depuis un an les connexions de confiance (OAuth) et des erreurs de configuration dans les environnements Salesforce. Ces attaques ne reposent pas sur des vulnérabilités logicielles, mais sur l'abus de privilèges déjà accordés aux applications tierces.

#### Points clés
* **Absence d'exploit technique :** Les attaquants n'utilisent aucun malware ni faille de sécurité classique, rendant les activités indétectables par les outils de surveillance d'authentification standards.
* **Ciblage des intégrations :** Les pirates détournent la confiance accordée aux applications tierces (vendors) pour exfiltrer massivement des données CRM.
* **Impact sectoriel :** Des entreprises majeures de la vente au détail, de l'éducation et de l'industrie ont été touchées.

#### Vecteurs d'attaque
1. **Vishing (Phishing vocal) :** Les attaquants se font passer pour le support informatique pour convaincre les employés d'autoriser une application malveillante (souvent déguisée en « Data Loader ») via l'écran de consentement OAuth.
2. **Vol de jetons (Token Theft) :** Compromission de fournisseurs tiers (ex: Salesloft, Gainsight, Klue) pour dérober des jetons OAuth et accéder aux instances Salesforce de leurs clients.
3. **Configuration incorrecte du mode invité :** Exploitation de permissions excessives sur les sites *Experience Cloud* (via les endpoints Aura) permettant d'extraire des données sans authentification.

#### Vulnérabilités (CVE non applicables)
Il ne s'agit pas de CVE traditionnelles, mais de **défauts de gestion de la surface d'attaque SaaS** :
* **Sur-privilèges :** Applications tierces disposant de scopes OAuth trop larges.
* **Shadow IT/Legacy :** Comptes de test ou intégrations obsolètes oubliés et toujours actifs.
* **Logique métier :** Paramétrage laxiste des accès invités (Guest User) permettant l'accès à des API internes.

#### Recommandations
* **Inventaire et gouvernance :** Auditer régulièrement les applications connectées, supprimer celles inutilisées depuis plus de 90 jours et appliquer le principe du moindre privilège sur les scopes OAuth.
* **Surveillance accrue :** Activer le framework *Real-Time Event Monitoring* de Salesforce et intégrer les logs dans une solution de type SIEM ou *Defender for Cloud Apps* pour détecter des comportements anormaux au niveau des API.
* **Sécurisation des accès invités :** Durcir les permissions des sites *Experience Cloud* pour limiter l'exposition des données.
* **Culture de sécurité :** Sensibiliser les employés à ne jamais valider de consentements OAuth sur demande téléphonique sans vérification via un canal officiel connu.

---
[Source](https://thehackernews.com/2026/07/microsoft-maps-year-long-shinyhunters.html){:target="_blank"}
