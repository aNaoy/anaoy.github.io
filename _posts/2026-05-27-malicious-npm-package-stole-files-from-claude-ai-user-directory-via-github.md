---
title: 'Malicious npm Package Stole Files From Claude AI User Directory via GitHub'
date: 2026-05-27
permalink: /posts/2026/05/27/malicious-npm-package-stole-files-from-claude-ai-user-directory-via-github/
tags:
- veille-cyber
- hackernews
---
### Exfiltration de données via le paquet npm malveillant "Malware-Slop"

Des chercheurs en cybersécurité ont identifié un paquet npm malveillant baptisé `mouse5212-super-formatter`, conçu pour dérober des fichiers sensibles. Cette campagne, nommée « Malware-Slop », cible spécifiquement le répertoire `/mnt/user-data` utilisé par l'outil d'IA Claude d'Anthropic.

**Points clés :**
* **Fonctionnement :** Le script se fait passer pour un utilitaire de synchronisation de déploiement. Lors de son installation (phase `postinstall`), il exploite des jetons GitHub (présents localement ou codés en dur) pour transférer récursivement les fichiers de la victime vers un dépôt GitHub contrôlé par l'attaquant.
* **Dissimulation :** Le logiciel malveillant génère de faux journaux de « connexion réseau » pour masquer l'exfiltration de données et utilise des dossiers nommés aléatoirement pour organiser les fichiers volés.
* **Négligence opérationnelle :** L'attaquant a involontairement divulgué ses propres jetons d'accès GitHub, suggérant une automatisation de la création de malware par IA sans respect des bonnes pratiques de sécurité (OPSEC).
* **Impact :** Le paquet a été téléchargé près de 676 fois. Bien que le compte GitHub associé ait été supprimé, cela souligne la montée en puissance de codes malveillants « bâclés » facilités par l'IA générative.

**Vulnérabilités :**
* Aucune CVE n'a été attribuée à ce jour, car il s'agit d'une campagne de type **Supply Chain Attack** (attaque par chaîne d'approvisionnement) utilisant un paquet malveillant légitime en apparence.

**Recommandations :**
* **Audit des dépendances :** Vérifier systématiquement les paquets npm ajoutés aux projets, en privilégiant des sources connues et auditées.
* **Gestion des jetons :** Ne jamais laisser de jetons GitHub ou d'identifiants sensibles dans les environnements de développement ou les configurations accessibles par des scripts tiers.
* **Principe du moindre privilège :** Restreindre les accès en écriture et en lecture des scripts de build aux seuls répertoires strictement nécessaires à leur exécution.
* **Surveillance :** Surveiller les processus suspects durant l'installation de dépendances (hooks `postinstall`) qui tentent d'effectuer des connexions réseau sortantes non sollicitées.

---
[Source](https://thehackernews.com/2026/05/malicious-npm-package-stole-files-from.html){:target="_blank"}
