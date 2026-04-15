---
title: 'Signed software abused to deploy antivirus-killing scripts'
date: 2026-04-15
permalink: /posts/2026/04/15/signed-software-abused-to-deploy-antivirus-killing-scripts/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne de malwares déguisés en logiciels publicitaires désactivant les antivirus

Une vaste campagne malveillante exploitant des outils légitimes signés numériquement par « Dragon Boss Solutions LLC » a été identifiée. Ces logiciels, présentés comme des navigateurs (ex: Chromstera, Chromnius), utilisent le mécanisme de mise à jour d'Advanced Installer pour déployer des charges utiles avec des privilèges SYSTEM, compromettant plus de 23 500 hôtes dans 124 pays, dont des infrastructures critiques (santé, énergie, gouvernement).

**Points clés :**
* **Vecteur d'attaque :** Utilisation détournée du système de mise à jour d'Advanced Installer pour une exécution silencieuse sans interaction utilisateur.
* **Neutralisation de la sécurité :** Le script *ClockRemoval.ps1* est utilisé pour identifier, arrêter et désinstaller divers produits antivirus (Malwarebytes, Kaspersky, McAfee, ESET).
* **Persistance :** Le malware modifie le fichier *hosts* pour bloquer les domaines des éditeurs de sécurité et configure des tâches récurrentes (toutes les 30 minutes) pour empêcher toute réactivation.
* **Risque critique :** L'infrastructure de mise à jour était non sécurisée (domaines non enregistrés), permettant théoriquement à n'importe quel acteur de prendre le contrôle total des machines infectées.

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur l'abus de fonctionnalités légitimes (design flaw du processus de mise à jour) et l'exécution de scripts PowerShell à haut privilège.

**Recommandations :**
* **Détection :** Rechercher les abonnements aux événements WMI contenant « MbRemoval » ou « MbSetup » et les tâches planifiées référençant « WMILoad » ou « ClockRemoval ».
* **Analyse système :** Auditer le fichier *hosts* pour détecter des redirections vers 0.0.0.0 liées à des éditeurs de sécurité.
* **Nettoyage :** Identifier et supprimer tout processus ou exécutable signé par « Dragon Boss Solutions LLC ».
* **Surveillance :** Vérifier les exclusions Microsoft Defender à la recherche de répertoires suspects (« DGoogle », « EMicrosoft », « DDapps »).

---
[Source](https://www.bleepingcomputer.com/news/security/signed-software-abused-to-deploy-antivirus-killing-scripts/){:target="_blank"}
