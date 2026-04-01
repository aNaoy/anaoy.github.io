---
title: 'Google Attributes Axios npm Supply Chain Attack to North Korean Group UNC1069'
date: 2026-04-01
permalink: /posts/2026/04/01/google-attributes-axios-npm-supply-chain-attack-to-north-korean-group-unc1069/
tags:
- veille-cyber
- hackernews
---
### Compromission de la Supply Chain : L'attaque du paquet npm Axios

Le groupe nord-coréen **UNC1069** a compromis le célèbre paquet npm *Axios* en prenant le contrôle du compte de son mainteneur. Cette attaque de chaîne d'approvisionnement injecte une dépendance malveillante, *plain-crypto-js*, pour déployer le logiciel malveillant **WAVESHAPER.V2**, un backdoor multiplateforme (Windows, macOS, Linux).

**Points clés :**
* **Vecteur d'attaque :** Utilisation d'un "postinstall hook" dans le fichier `package.json` pour une exécution automatique et furtive lors de l'installation.
* **Charge utile :** Un dropper JavaScript (SILKBELL) télécharge des backdoors spécifiques selon l'OS (PowerShell pour Windows, binaire Mach-O pour macOS, Python pour Linux).
* **Capacités :** Le malware WAVESHAPER.V2 permet d'exécuter des commandes système, de lister des répertoires et d'injecter des binaires arbitraires.
* **Indicateurs :** Les versions compromises sont la **1.14.1** et la **0.30.4**.

**Vulnérabilités :**
* Aucune CVE n'est associée à ce jour, car l'attaque exploite une compromission de compte tiers et les mécanismes légitimes de gestionnaire de paquets (`npm`).

**Recommandations :**
* **Audit immédiat :** Vérifier l'arbre des dépendances pour détecter les versions 1.14.1 ou 0.30.4 d'Axios ou la présence de `plain-crypto-js`.
* **Remédiation :** Rétrograder vers une version sécurisée d'Axios et verrouiller la dépendance dans `package-lock.json`.
* **Isolation :** Isoler les systèmes compromis, supprimer les processus malveillants et procéder à une rotation complète des identifiants (secrets) exposés sur ces machines.
* **Filtrage réseau :** Bloquer les communications vers le serveur C2 identifié (`sfrclak[.]com` / `142.11.206.73`).
* **Sécurité globale :** Étendre l'audit à tous les gestionnaires de paquets utilisés (PyPI, NuGet, etc.) dans les pipelines de build, car cette méthode est hautement scalable.

---
[Source](https://thehackernews.com/2026/04/google-attributes-axios-npm-supply.html){:target="_blank"}
