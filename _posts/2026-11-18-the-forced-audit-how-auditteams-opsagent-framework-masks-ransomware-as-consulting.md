---
title: 'The forced audit: how AuditTeam’s OpsAgent framework masks ransomware as consulting'
date: 2026-11-18
permalink: /posts/2026/11/18/the-forced-audit-how-auditteams-opsagent-framework-masks-ransomware-as-consulting/
tags:
- veille-cyber
- securelist
---
### Analyse de la campagne cybercriminelle "AuditTeam" et du framework OpsAgent

Le groupe "AuditTeam" déploie depuis janvier 2026 une campagne de ransomware sophistiquée ciblant des organisations à travers le monde. Sous couvert de fournir des rapports de vulnérabilités, le groupe exige le paiement d'une "taxe d'audit et de conseil" pour éviter la divulgation de données volées, tout en procédant au chiffrement des fichiers.

**Points clés :**
* **Évolution technique :** Le framework utilisé, *OpsAgent*, a migré du C++ vers Rust, intégrant des fonctionnalités avancées comme les shells interactifs et des communications WebSocket chiffrées (TLS).
* **Mode opératoire :** L'utilisation d'outils modulaires permet une injection de code (via *named pipes* ou injection directe) et un pilotage à distance via des sous-domaines Amazon CloudFront.
* **Développement assisté par IA :** La structure uniforme du code et la résolution dynamique des fonctions suggèrent l'usage d'outils d'assistance à la génération de code pour accélérer le développement des modules.

**Vulnérabilités et vecteurs d'attaque :**
* **Désactivation des protections :** Utilisation d'un pilote légitime (Beijing Jiangmin Antivirus) numériquement signé pour désactiver environ 220 produits de sécurité, outils de monitoring (Sysmon, Splunk, Wazuh) et services de sauvegarde (Veeam, Acronis).
* **Mise à jour C2 :** Le framework exploitait initialement un dépôt GitHub public pour récupérer ses domaines de commande et contrôle (C2), facilitant le déploiement et la rotation des infrastructures.
* **Absence de CVE spécifique :** L'article ne mentionne pas de CVE particulière, car le framework repose sur des techniques d'injection de code standard (process hollowing, manipulation de jetons, *pass-the-hash*) et des abus de fonctionnalités système légitimes.

**Recommandations de sécurité :**
* **Surveillance des processus :** Détecter les injections de code dans des processus tiers (ex: `msiexec.exe`, `notepad.exe`) et surveiller le chargement de pilotes non autorisés, même s'ils sont signés.
* **Filtrage réseau :** Bien que le blocage IP soit inefficace en raison de l'usage de CDN (CloudFront), restreindre les connexions sortantes vers des dépôts publics suspects et surveiller les flux WebSocket inhabituels.
* **Protection des terminaux :** Renforcer la protection des services de sauvegarde et des bases de données (SQL, Redis, MongoDB) qui sont des cibles prioritaires pour le module de chiffrement.
* **Forensique :** En cas d'infection, rechercher les indicateurs spécifiques comme le fichier `syscache.dat` utilisé par le malware et vérifier l'intégrité des clichés instantanés (*shadow copies*).

---
[Source](https://securelist.com/auditteam-opsagent-forced-audit/122031/){:target="_blank"}
