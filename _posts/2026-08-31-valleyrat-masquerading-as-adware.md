---
title: 'ValleyRAT masquerading as adware'
date: 2026-08-31
permalink: /posts/2026/08/31/valleyrat-masquerading-as-adware/
tags:
- veille-cyber
- securelist
---
### ValleyRAT : La menace dissimulée derrière des logiciels publicitaires

Des attaquants utilisent des logiciels publicitaires (adware) légitimes et signés numériquement, tels que *QN Wallpaper*, pour distribuer le backdoor **ValleyRAT**. En exploitant la confiance des utilisateurs qui ajoutent ces outils aux exclusions de leurs antivirus, les assaillants déploient une chaîne d'infection complexe.

#### Points clés
*   **Vecteur d'attaque** : Utilisation d'installateurs trompeurs (affichant des outils légitimes comme DingTalk ou Chrome) pour masquer le déploiement du logiciel malveillant.
*   **Technique de persistance** : Utilisation du *DLL Sideloading* via `libcef.dll` pour exécuter du code malveillant sous un processus signé.
*   **Fonctionnalités du backdoor** :
    *   Espionnage (keylogger, capture du presse-papiers, captures d'écran).
    *   Vol d'informations système détaillées.
    *   Capacité de téléchargement et d'exécution de modules supplémentaires (via *process hollowing*).
    *   Mécanismes d'auto-protection avancés (détection d'outils d'analyse, injection dans `svchost.exe`, et marquage du processus comme "critique" pour provoquer un BSOD en cas d'arrêt).
*   **Attribution** : La campagne est attribuée au groupe **Silver Fox**, ciblant principalement l'Inde et la Chine (plus de 100 000 détections).

#### Vulnérabilités exploitées
*   **DLL Sideloading** : Chargement de bibliothèques malveillantes par des processus légitimes.
*   **Désactivation des protections** : Utilisation de la clé de registre `DisableAntiSpyware` pour neutraliser Windows Defender.
*   **Élévation de privilèges** : Utilisation de l'utilitaire `runas` pour obtenir des droits d'administrateur.

#### Recommandations
*   **Gestion des exclusions** : Ne jamais ajouter de logiciels douteux ou d'adwares aux listes d'exclusion des solutions de sécurité.
*   **Politique logicielle** : Restreindre strictement l'installation de logiciels tiers sur les postes de travail professionnels.
*   **Sensibilisation** : Former les utilisateurs à ne pas télécharger d'applications provenant de sources non officielles ou douteuses, souvent déguisées en outils de productivité.
*   **Surveillance** : Surveiller les activités réseau suspectes et les modifications de registres (notamment `autorun` et `DisableAntiSpyware`).

---
[Source](https://securelist.com/valleyrat-backdoor-adware/121175/){:target="_blank"}
