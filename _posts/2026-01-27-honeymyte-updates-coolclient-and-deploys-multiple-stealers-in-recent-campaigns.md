---
title: 'HoneyMyte updates CoolClient and deploys multiple stealers in recent campaigns'
date: 2026-01-27
permalink: /posts/2026/01/27/honeymyte-updates-coolclient-and-deploys-multiple-stealers-in-recent-campaigns/
tags:
- veille-cyber
- securelist
---
**Veille Technologique : Évolutions et Tactiques du Groupe HoneyMyte**

Le groupe de menace évoluée (APT) HoneyMyte, également connu sous les noms de Mustang Panda ou Bronze President, maintient une activité soutenue, ciblant principalement des entités gouvernementales en Asie et en Europe. Les récentes campagnes révèlent une évolution de leurs outils, notamment une mise à jour significative du cheval de Troie CoolClient et le déploiement de plusieurs voleurs d'informations de connexion de navigateurs.

**Points Clés :**

*   **Évolution de CoolClient :** La dernière version du cheval de Troie CoolClient intègre de nouvelles fonctionnalités tout en conservant celles de base comme la collecte d'informations système, l'envoi de fichiers, la journalisation des frappes, le tunneling TCP et l'exécution de modules en mémoire. De nouvelles capacités incluent la surveillance du presse-papiers et le vol d'identifiants de proxy HTTP.
*   **Techniques d'Évasion :** Le groupe continue d'abuser du chargement de DLL (DLL sideloading) en utilisant des exécutables signés de logiciels légitimes tels que Sangfor, BitDefender ou VLC Media Player. Il utilise également des techniques de contournement de l'UAC (User Account Control).
*   **Nouveaux Outils de Vol d'Informations :** HoneyMyte déploie plusieurs variants d'un voleur d'informations de connexion de navigateurs, ciblant spécifiquement Chrome, Microsoft Edge et d'autres navigateurs basés sur Chromium. Ces outils extraient les identifiants enregistrés, y compris les mots de passe chiffrés.
*   **Scripts de Reconnaissance et d'Exfiltration :** Le groupe utilise des scripts batch et PowerShell pour la collecte d'informations système détaillées, la recherche et l'exfiltration de documents sensibles, ainsi que le vol d'identifiants de navigateurs. L'utilisation de services de partage de fichiers publics comme Pixeldrain est notable pour l'exfiltration de données.
*   **Élargissement des Objectifs :** Les capacités actuelles de HoneyMyte vont au-delà de la simple espionnage, incluant la surveillance active de l'activité utilisateur par la capture de frappes, la copie de données du presse-papiers et le vol d'identifiants.

**Vulnérabilités et Vecteurs d'Attaque Connus :**

*   **DLL Sideloading :** Exploitation de binaires légitimes pour charger des bibliothèques DLL malveillantes.
*   **Contournement de l'UAC :** Techniques permettant d'obtenir des privilèges élevés sans l'intervention de l'utilisateur.
*   **Vol d'Identifiants de Navigateur :** Accès direct aux bases de données de mots de passe enregistrés et aux clés de déchiffrement.
*   **Exfiltration via des Services Publics :** Utilisation de plateformes comme Pixeldrain.com et Google Drive pour la dissimulation des transferts de données.

**Recommandations :**

*   **Surveillance et Détection :** Maintenir une vigilance accrue quant au déploiement de la panoplie d'outils de HoneyMyte, y compris CoolClient, ToneShell, PlugX, Qreverse et LuminousMoth.
*   **Gestion des Privilèges :** Appliquer rigoureusement les principes du moindre privilège pour limiter l'impact des actions malveillantes après une compromission.
*   **Sécurisation des Terminaux :** Renforcer les défenses sur les points d'accès, notamment via des solutions antivirus et anti-malware à jour, et surveiller les tentatives d'exécution de code suspect.
*   **Formation des Utilisateurs :** Sensibiliser les utilisateurs aux risques liés au phishing, à l'ingénierie sociale et à l'exécution de fichiers suspects.
*   **Mise à Jour des Logiciels :** S'assurer que tous les logiciels, en particulier ceux qui sont couramment ciblés pour le DLL sideloading (navigateurs, lecteurs multimédias, outils d'entreprise), sont maintenus à jour.
*   **Surveillance du Trafic Réseau :** Inspecter le trafic réseau pour détecter des communications anormales avec des serveurs de commande et de contrôle potentiels, ainsi que des exfiltrations de données inhabituelles.

---
[Source](https://securelist.com/honeymyte-updates-coolclient-uses-browser-stealers-and-scripts/118664/){:target="_blank"}
