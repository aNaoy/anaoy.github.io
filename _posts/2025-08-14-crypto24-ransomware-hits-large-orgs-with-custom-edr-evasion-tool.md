---
title: 'Crypto24 ransomware hits large orgs with custom EDR evasion tool'
date: 2025-08-14
permalink: /posts/2025/08/14/crypto24-ransomware-hits-large-orgs-with-custom-edr-evasion-tool/
tags:
- veille-cyber
- bleepingcomp
---
## Crypto24 : Évasion Avancée des Systèmes de Sécurité

Le groupe de ransomware Crypto24 cible des organisations de grande taille dans les secteurs de la finance, de la fabrication, du divertissement et de la technologie à travers les États-Unis, l'Europe et l'Asie. Ce groupe, potentiellement composé d'anciens membres d'opérations de ransomware disparues, utilise des outils sur mesure pour réussir ses attaques.

Après avoir obtenu un accès initial, Crypto24 s'établit discrètement en activant des comptes administratifs existants ou en créant de nouveaux comptes locaux. Une phase de reconnaissance permet d'identifier les ressources système, suivie de la création de services Windows malveillants et de tâches planifiées pour assurer la persistance. Parmi ces outils, WinMainSvc agit comme un enregistreur de frappe (keylogger) et MSRuntime comme chargeur de ransomware.

La particularité de Crypto24 réside dans son utilisation d'une version modifiée de l'outil open-source RealBlindingEDR. Cet outil est conçu pour désactiver les pilotes de sécurité de plusieurs éditeurs de solutions de cybersécurité majeurs, notamment Trend Micro, Kaspersky, Sophos, SentinelOne, Malwarebytes, Cynet, McAfee, Bitdefender, Broadcom (Symantec), Cisco, Fortinet et Acronis. Il parvient à cela en identifiant les pilotes via leurs métadonnées et en désactivant leurs hooks au niveau du noyau, rendant ainsi les moteurs de détection "aveugles".

Dans le cas des produits Trend Micro, si les attaquants disposent de privilèges d'administrateur, ils exécutent un script qui utilise l'utilitaire légitime `XBCUninstaller.exe` pour désinstaller Trend Vision One. Ce processus, orchestré par `gpscript.exe`, empêche la détection des charges utiles ultérieures comme le keylogger et le ransomware.

Le keylogger, se faisant passer pour "Microsoft Help Manager", enregistre les titres des fenêtres actives ainsi que toutes les frappes au clavier. Les attaquants utilisent également les partages SMB pour leurs déplacements latéraux et le staging des données avant leur exfiltration. Les données volées sont envoyées vers Google Drive via un outil personnalisé exploitant l'API WinINET.

Avant d'exécuter la charge utile du ransomware, Crypto24 supprime les copies de volume (shadow copies) afin de rendre la récupération des fichiers plus difficile. Bien que les détails spécifiques du ransomware, tels que le schéma de chiffrement ou les notes de rançon, ne soient pas divulgués, des indicateurs de compromission sont mis à disposition pour aider les professionnels de la sécurité à détecter et bloquer ces attaques.

### Points Clés :

*   **Opérations furtives :** Utilisation d'outils personnalisés pour l'évasion des systèmes de sécurité.
*   **Persistance :** Création de services Windows malveillants (keylogger, chargeur de ransomware) et de tâches planifiées.
*   **Évasion avancée :** Modification de RealBlindingEDR pour désactiver les pilotes de sécurité de multiples fournisseurs.
*   **Désinstallation d'agents :** Utilisation d'un utilitaire légitime pour désinstaller les solutions de sécurité ciblées.
*   **Exfiltration de données :** Envoi des données vers Google Drive via un outil customisé.
*   **Préparation au chiffrement :** Suppression des shadow copies avant le déploiement du ransomware.

### Vulnérabilités Exploités :

*   Pas de CVE spécifiques mentionnés directement dans l'article.
*   L'exploitation de RealBlindingEDR cible la fonctionnalité des pilotes de sécurité des solutions EDR.
*   L'utilisation d'un utilitaire de désinstallation légitime (`XBCUninstaller.exe`) exploite les privilèges élevés des attaquants.

### Recommandations :

*   Mise en place de mesures pour détecter et bloquer les activités liées aux indicateurs de compromission (IoC) fournis.
*   Surveillance attentive de la création de services Windows non autorisés et de tâches planifiées.
*   Renforcement des permissions et des contrôles d'accès pour empêcher l'utilisation abusive d'outils légitimes.
*   Mise à jour régulière des solutions de sécurité et des systèmes d'exploitation.
*   Formation des employés aux bonnes pratiques de cybersécurité pour prévenir l'accès initial.

---
[Source](https://www.bleepingcomputer.com/news/security/crypto24-ransomware-hits-large-orgs-with-custom-edr-evasion-tool/){:target="_blank"}
