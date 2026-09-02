---
title: 'Hackers abuse Faronics Deploy admin tool to install ScreenConnect'
date: 2026-09-02
permalink: /posts/2026/09/02/hackers-abuse-faronics-deploy-admin-tool-to-install-screenconnect/
tags:
- veille-cyber
- bleepingcomp
---
### Détournement de la plateforme Faronics Deploy pour un accès distant illicite

Des acteurs malveillants exploitent la plateforme légitime de gestion de parc informatique **Faronics Deploy** pour prendre le contrôle à distance de systèmes via des campagnes de phishing.

**Points clés :**
* **Vecteur d'attaque :** Des emails de phishing (factures, documents fiscaux) incitent les victimes à télécharger un installeur Faronics légitime, déguisé en logiciel Adobe ou mise à jour de plugin.
* **Mode opératoire :** Une fois l'agent Faronics installé et l'appareil enrôlé sous leur contrôle, les attaquants utilisent les fonctionnalités natives de déploiement pour exécuter des scripts PowerShell (`curl`, `mshta`, `msiexec`).
* **Objectif final :** L'installation de **ScreenConnect**, un outil de prise en main à distance, offrant aux attaquants un canal d'accès persistant et indépendant de Faronics.
* **Statut :** La menace a nettement diminué suite aux mesures correctives mises en œuvre par l'éditeur Faronics en août.

**Vulnérabilités :**
* Aucune CVE n'est associée à cet incident, car il s'agit d'un **détournement d'usage d'un outil légitime (Living-off-the-land)**.

**Recommandations pour les administrateurs :**
* **Audit des logs :** Vérifier le fichier `C:\ProgramData\Faronics\Logs\ScriptRunner.log` pour détecter des exécutions de scripts suspects ou des URLs de téléchargement inhabituelles.
* **Analyse des configurations :** Inspecter le paramètre `ck` dans les requêtes de configuration Faronics pour identifier des déploiements ou comptes compromis.
* **Détection d'outils :** Rechercher toute installation non autorisée ou non planifiée de l'agent **ScreenConnect** sur les endpoints du réseau.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-abuse-faronics-deploy-admin-tool-to-install-screenconnect/){:target="_blank"}
