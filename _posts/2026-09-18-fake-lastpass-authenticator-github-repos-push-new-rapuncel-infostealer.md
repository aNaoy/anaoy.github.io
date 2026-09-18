---
title: 'Fake LastPass Authenticator GitHub repos push new Rapuncel infostealer'
date: 2026-09-18
permalink: /posts/2026/09/18/fake-lastpass-authenticator-github-repos-push-new-rapuncel-infostealer/
tags:
- veille-cyber
- bleepingcomp
---
### Menace Rapuncel : Campagne de vol de données via des dépôts GitHub compromis

Une campagne de cyberattaques utilisant le SEO pour optimiser le référencement de faux dépôts GitHub usurpe l'identité de marques logicielles renommées, dont LastPass, pour diffuser un nouveau logiciel malveillant de vol d'informations : **Rapuncel**.

**Points clés :**
* **Vecteur d'attaque :** Téléchargement de fichiers ZIP "gonflés" (jusqu'à 148 Mo) pour contourner l'analyse des solutions de sécurité.
* **Installation :** Utilisation d'une copie légitime de l'outil `vsdbg.exe` (Microsoft Visual Studio) configurée pour charger une DLL malveillante.
* **Neutralisation des défenses :** Déploiement d'un pilote noyau (`Alinubx.sys`), signé par Microsoft, capable de terminer 145 processus antivirus et EDR en contournant la protection *Protected Process Light* (PPL).
* **Vol de données :** Une fois les défenses désactivées, le malware exfiltre les identifiants de 25 navigateurs, 30 portefeuilles crypto, les sessions (Discord, Steam, Telegram), les documents sensibles, les captures d'écran et les informations système.
* **Persistance :** Le malware s'installe en tant que service Windows pour garantir sa réexécution après un redémarrage.

**Vulnérabilités :**
* Le pilote malveillant (`Alinubx.sys`) profite d'une signature légitime via la chaîne de publication matérielle Windows. 
* *Note : Aucune CVE spécifique n'est associée à cette campagne, car elle repose sur l'abus de composants légitimes et de pilotes signés non répertoriés dans la liste de blocage de Microsoft.*

**Recommandations :**
* **Vérification des sources :** Télécharger uniquement les logiciels depuis les sites officiels des éditeurs.
* **Méfiance sur GitHub :** Être vigilant face aux dépôts suspects, même s'ils apparaissent dans les résultats de recherche sponsorisés ou optimisés.
* **Protection des terminaux :** S'assurer que les solutions de sécurité sont à jour et capables de détecter les comportements suspects liés au chargement de pilotes non signés ou malveillants.

---
[Source](https://www.bleepingcomputer.com/news/security/fake-lastpass-authenticator-github-repos-push-new-rapuncel-infostealer/){:target="_blank"}
