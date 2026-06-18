---
title: 'Police cleans nearly 15,000 SocGholish-infected sites tied to Evil Corp'
date: 2026-06-18
permalink: /posts/2026/06/18/police-cleans-nearly-15000-socgholish-infected-sites-tied-to-evil-corp/
tags:
- veille-cyber
- bleepingcomp
---
### Démantèlement de l'infrastructure SocGholish par les forces de l'ordre

Dans le cadre de l'opération internationale *Endgame*, des agences de police (Pays-Bas, États-Unis, Canada, Allemagne) ont neutralisé une infrastructure majeure utilisée par le groupe criminel russe **Evil Corp**. Cette intervention a permis d'assainir 14 971 sites WordPress compromis et de mettre hors service 106 serveurs liés au botnet SocGholish.

**Points clés :**
* **Nature de la menace :** SocGholish (aussi appelé FakeUpdates ou GhoLoader) est un téléchargeur de logiciels malveillants actif depuis 2017.
* **Mode opératoire :** Le malware détourne des sites légitimes (principalement sous WordPress) pour inciter les visiteurs à télécharger des mises à jour de navigateur factices.
* **Impact :** Une fois installé, le malware ouvre une porte dérobée permettant de déployer d'autres menaces, notamment des ransomwares comme WastedLocker, Hades, ou Phoenix CryptoLocker.
* **Vulnérabilités :** L'article ne cite pas de CVE spécifique, car l'attaque repose principalement sur l'exploitation des vulnérabilités des sites WordPress mal sécurisés et sur l'ingénierie sociale visant les utilisateurs finaux.

**Recommandations pour les administrateurs WordPress :**
* **Gestion des accès :** Modifier immédiatement tous les identifiants de connexion et activer l'authentification multifacteur (MFA).
* **Audit de sécurité :** Supprimer tout compte utilisateur inconnu ou suspect sur l'interface d'administration.
* **Maintenance :** Maintenir le CMS, les thèmes et les extensions systématiquement à jour pour combler les failles de sécurité exploitées par les attaquants.

---
[Source](https://www.bleepingcomputer.com/news/security/law-enforcement-nukes-socgholish-malware-from-nearly-15-000-sites/){:target="_blank"}
