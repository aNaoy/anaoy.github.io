---
title: '7-Eleven confirms data breach claimed by the ShinyHunters gang'
date: 2026-05-19
permalink: /posts/2026/05/19/7-eleven-confirms-data-breach-claimed-by-the-shinyhunters-gang/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite de données massive chez 7-Eleven orchestrée par ShinyHunters

La chaîne de distribution 7-Eleven a confirmé une intrusion dans ses systèmes informatiques survenue le 8 avril 2026, impliquant le vol de documents internes. Le groupe de cybercriminels **ShinyHunters** a revendiqué l'attaque, affirmant avoir exfiltré plus de 600 000 enregistrements contenant des données d'entreprise et des informations personnelles identifiables (PII) via une compromission de l'environnement Salesforce de l'enseigne. Après le refus de 7-Eleven de verser une rançon, le groupe a publié une archive de 9,4 Go de données sur le dark web.

**Points clés :**
* **Nature de l'attaque :** Accès non autorisé à des systèmes de stockage de documents liés aux franchisés.
* **Impact :** Exfiltration massive de données clients et d'entreprise via l'environnement Salesforce.
* **Contexte :** ShinyHunters mène une campagne active ciblant spécifiquement les clients de la plateforme Salesforce (précédemment impliqué dans les attaques *Salesforce Aura*).
* **Réponse :** 7-Eleven a lancé une enquête interne et notifié les autorités ainsi que les personnes affectées.

**Vulnérabilités :**
* L'attaque exploite des vulnérabilités ou des failles de configuration dans l'intégration **Salesforce** de l'entreprise. Aucune CVE spécifique n'a été attribuée à cette intrusion, le vecteur d'attaque s'inscrivant dans une campagne plus large ciblant les accès SaaS.

**Recommandations :**
* **Ne pas payer la rançon :** Le FBI déconseille formellement le paiement, car cela ne garantit ni la suppression des données volées ni l'arrêt des tentatives d'extorsion futures.
* **Sécurisation des environnements SaaS :** Renforcer les contrôles d'accès (MFA robuste), auditer les configurations des plateformes tierces (Salesforce) et surveiller étroitement les accès aux API.
* **Réponse aux incidents :** Les entreprises utilisant des plateformes cloud centralisées doivent valider leurs surfaces d'exposition pour détecter les mouvements latéraux et les accès non autorisés avant que l'exfiltration ne soit complète.

---
[Source](https://www.bleepingcomputer.com/news/security/7-eleven-confirms-data-breach-claimed-by-the-shinyhunters-gang/){:target="_blank"}
