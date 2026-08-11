---
title: 'Project CAV3RN continues: Google Apps Script as C2 relay and DNS-based C2 channel selection'
date: 2026-08-11
permalink: /posts/2026/08/11/project-cav3rn-continues-google-apps-script-as-c2-relay-and-dns-based-c2-channel-selection/
tags:
- veille-cyber
- securelist
---
### Évolution et mécanismes du framework d'espionnage Project CAV3RN

Le framework d'espionnage **Project CAV3RN** continue d'évoluer avec l'introduction de composants modulaires sophistiqués, visant principalement des cibles en Israël. Sa nouvelle architecture se distingue par une gestion dynamique du centre de commande et de contrôle (C2) et une modularité permettant des mises à jour à chaud.

#### Points clés
*   **Stratégie de communication hybride :** Le framework utilise des requêtes DNS (enregistrements A) pour décider, en temps réel, de la méthode de communication la plus appropriée : HTTPS direct ou un relais via *Google Apps Script*.
*   **Contrôle via DNS :** Le DNS sert de plan de contrôle. Il permet non seulement de basculer entre les canaux C2, mais aussi de mettre à jour dynamiquement l'ID de déploiement *Google Apps Script*, rendant l'infrastructure très résiliente.
*   **Broker local :** Un composant nommé `rnp.dll` (masqué en bibliothèque OpenPGP) orchestre les différents modules DLL, gère les communications inter-composants et permet l'ajout ou la mise à jour de fonctionnalités sans redémarrer le processus hôte.
*   **Persistance et camouflage :** L'usage de services légitimes comme *Google Apps Script* permet de noyer le trafic malveillant dans le trafic réseau habituel, rendant la détection réseau particulièrement complexe.

#### Vulnérabilités
Bien qu'aucune CVE spécifique ne soit citée (il s'agit d'une menace ciblée utilisant des services légitimes), les vulnérabilités exploitées sont de nature architecturale :
*   **Abus de confiance :** Utilisation détournée de services cloud (Google Apps Script).
*   **Architecture modulaire :** Le chargement dynamique de DLL non signées ou non vérifiées via le broker local permet une exécution de code arbitraire et des mises à jour malveillantes silencieuses.
*   **Redirection DNS :** L'infrastructure repose sur un domaine potentiellement détourné (`studiotikva[.]com`) pour diriger les flux vers des serveurs contrôlés par les attaquants.

#### Recommandations
*   **Surveillance réseau :** Surveiller les requêtes DNS inhabituelles vers des domaines suspects ou générés dynamiquement, notamment celles incluant des chaînes codées en hexadécimal.
*   **Analyse du trafic :** Inspecter le trafic HTTPS vers `script.google[.]com` et vérifier les en-têtes personnalisés (ex: `X-Client-Id`) qui ne correspondent pas à une activité utilisateur normale.
*   **Contrôle des DLL :** Implémenter des politiques de contrôle d'application (AppLocker ou EDR) pour empêcher le chargement de bibliothèques non signées ou situées dans des répertoires suspects.
*   **Analyse de comportement :** Surveiller l'activité de processus créant des DLL et scannant les répertoires locaux de manière répétée, comportement typique du broker `rnp.dll`.
*   **Gestion des logs :** Être vigilant face aux outils de diagnostic activés via des commandes comme `s_enLog`, souvent utilisées par les attaquants pour le débogage de leurs propres composants.

---
[Source](https://securelist.com/project-cav3rn-continues/120991/){:target="_blank"}
