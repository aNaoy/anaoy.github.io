---
title: 'Bitter Hackers Deploy New PapRAT Backdoor in Cyberespionage Campaign Targeting South Asia'
date: 2026-11-09
permalink: /posts/2026/11/09/bitter-hackers-deploy-new-paprat-backdoor-in-cyberespionage-campaign-targeting-south-asia/
tags:
- veille-cyber
- hackernews
---
### Menace persistante : Le groupe Bitter déploie le nouveau backdoor PapRAT

Le groupe de cyberespionnage Bitter (APT-C-08) a lancé une nouvelle campagne ciblant des organisations en Asie du Sud, utilisant un cheval de Troie d'accès à distance (RAT) inédit baptisé **PapRAT**. Ce malware, développé en C++ et en Rust, permet un contrôle complet des systèmes infectés et s'appuie sur des techniques sophistiquées "Living-off-the-Land" (LotL) pour minimiser son empreinte.

**Points clés :**
* **Polyvalence du malware :** PapRAT exécute des commandes système, capture des captures d'écran, gère des fichiers (upload/download/suppression) et réalise une énumération exhaustive des disques et répertoires. La version Rust permet en outre l'exécution directe de scripts PowerShell.
* **Stratégie de déploiement :** Le groupe utilise trois chaînes d'infection distinctes pour contourner la détection, exploitant des fichiers LNK, des images disques VHDX, des raccourcis URL (via WebDAV) et des installateurs MSI.
* **Flexibilité opérationnelle :** Les attaquants utilisent des serveurs de commande et de contrôle (C2) pour mettre à jour les instructions côté serveur, évitant ainsi le téléchargement de nouveaux binaires détectables.
* **Persistance :** La campagne peut également déployer le malware WmRAT, déjà associé au groupe Bitter.

**Vulnérabilités :**
Aucune CVE spécifique n'est exploitée ; l'attaque repose sur l'abus de fonctionnalités natives de Windows (LotL) :
* Utilisation détournée de `ftp.exe`, `curl.exe` et des planificateurs de tâches.
* Abus de l'exécution automatique via des fichiers `.lnk`, `.url`, `.vhdx` et `.msi`.

**Recommandations :**
* **Surveillance proactive :** Surveiller les comportements suspects liés aux outils de script, à la création de tâches planifiées et à l'exécution de packages MSI inhabituels.
* **Gestion des accès et fichiers :** Faire preuve d'une grande prudence face aux fichiers LNK, URL, images disques (VHDX) ou installateurs MSI reçus via des canaux non sollicités.
* **Défense en profondeur :** Ne pas se reposer uniquement sur la détection de signatures de malwares connus ; privilégier l'analyse comportementale et le blocage des exécutions non autorisées via des politiques de contrôle d'application (AppLocker ou équivalent).

---
[Source](https://thehackernews.com/2026/11/bitter-hackers-deploy-new-paprat.html){:target="_blank"}
