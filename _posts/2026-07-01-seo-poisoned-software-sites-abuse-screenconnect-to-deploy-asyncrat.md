---
title: 'SEO-Poisoned Software Sites Abuse ScreenConnect to Deploy AsyncRAT'
date: 2026-07-01
permalink: /posts/2026/07/01/seo-poisoned-software-sites-abuse-screenconnect-to-deploy-asyncrat/
tags:
- veille-cyber
- hackernews
---
### Campagne de SEO-Poisoning : Distribution d'AsyncRAT via ScreenConnect

Une campagne de cyberattaques massive, multilingue et multi-domaines, exploite le référencement naturel (SEO) pour piéger les utilisateurs. En créant des sites web frauduleux imitant des logiciels populaires (tels qu'OBS Studio, DS4Windows ou Bandicam), les attaquants distribuent des archives malveillantes permettant de compromettre des postes de travail.

**Points clés :**
* **Vecteur d'attaque :** Utilisation du SEO pour placer des sites frauduleux en tête des moteurs de recherche (Google, Bing).
* **Méthode d'infection :** Les archives contiennent un binaire Microsoft légitime et une DLL malveillante, exploitant le **DLL side-loading** pour installer l'outil d'accès à distance **ScreenConnect**.
* **Persistance et exécution :** Une fois actif, ScreenConnect exécute des scripts PowerShell et VBScript pour désactiver les protections (Microsoft Defender, UAC), établir une tâche planifiée ("MasterPackager.Updater") et injecter **AsyncRAT** en mémoire via *process hollowing*.
* **Impact :** Les attaquants obtiennent un contrôle total, permettant le vol de données, la surveillance de l'activité utilisateur et l'enregistrement de l'écran.

**Vulnérabilités exploitées :**
* **DLL Side-Loading :** Chargement d'une bibliothèque malveillante par un binaire légitime signé.
* **Process Hollowing (Technique MITRE T1055.012) :** Injection de code malveillant dans un processus sain pour contourner la détection.
* *Note : Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur l'abus de fonctionnalités système et de logiciels légitimes.*

**Recommandations :**
* **Vigilance au téléchargement :** Ne télécharger des logiciels que depuis les sites officiels vérifiés et éviter les liens sponsorisés ou les résultats de recherche non confirmés.
* **Protection des endpoints :** Maintenir les solutions EDR/antivirus à jour pour détecter les comportements suspects (scripts PowerShell anormaux, modification des exclusions Defender).
* **Contrôle des privilèges :** Restreindre les droits d'administration sur les postes de travail pour limiter la capacité des scripts à modifier les paramètres de sécurité (UAC/Defender).
* **Surveillance système :** Surveiller les tâches planifiées suspectes et les processus de communication réseau inhabituels vers des domaines inconnus ou de type `.gd`.

---
[Source](https://thehackernews.com/2026/07/seo-poisoned-software-sites-abuse.html){:target="_blank"}
