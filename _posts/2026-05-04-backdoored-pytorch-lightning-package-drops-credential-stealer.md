---
title: 'Backdoored PyTorch Lightning package drops credential stealer'
date: 2026-05-04
permalink: /posts/2026/05/04/backdoored-pytorch-lightning-package-drops-credential-stealer/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de la chaîne d'approvisionnement du paquet PyTorch Lightning

Une version malveillante du framework d'apprentissage profond PyTorch Lightning (v2.6.3) a été diffusée sur le dépôt PyPI, contenant une chaîne d'exécution dissimulée capable de dérober des identifiants et des secrets sensibles.

**Points clés :**
*   **Mécanisme :** Lors de l'importation de la bibliothèque (`import lightning`), un processus en arrière-plan télécharge silencieusement l'environnement d'exécution JavaScript « Bun » pour exécuter une charge utile obfusquée de 11,4 Mo.
*   **Malware :** Identifié par Microsoft sous le nom « ShaiWorm », le logiciel malveillant cible les fichiers `.env`, les clés API, les jetons GitHub, ainsi que les données enregistrées dans les navigateurs (Chrome, Firefox, Brave).
*   **Impact :** Il permet également l'exécution de commandes système arbitraires et l'accès aux services cloud (AWS, Azure, GCP). Bien que l'attaque semble limitée, tout utilisateur ayant exécuté la version 2.6.3 est considéré comme compromis.
*   **Vulnérabilité :** Aucune CVE n'a été attribuée à ce jour ; il s'agit d'une compromission directe du pipeline de publication/build du paquet.

**Recommandations :**
*   **Nettoyage immédiat :** Si la version 2.6.3 a été installée, désinstallez-la et revenez à la version sécurisée (2.6.1).
*   **Rotation des secrets :** Considérant les secrets comme exposés, il est impératif d'effectuer une rotation immédiate de toutes les clés API, jetons d'accès (GitHub, cloud) et mots de passe stockés sur les machines ayant utilisé le paquet infecté.
*   **Audit :** Surveillez les logs système pour détecter toute activité inhabituelle liée à l'exécution de processus « Bun » ou à des exfiltrations réseau suspectes.

---
[Source](https://www.bleepingcomputer.com/news/security/backdoored-pytorch-lightning-package-drops-credential-stealer/){:target="_blank"}
