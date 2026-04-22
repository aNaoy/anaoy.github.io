---
title: 'Mustang Panda’s New LOTUSLITE Variant Targets India Banks, South Korea Policy Circles'
date: 2026-04-22
permalink: /posts/2026/04/22/mustang-pandas-new-lotuslite-variant-targets-india-banks-south-korea-policy-circles/
tags:
- veille-cyber
- hackernews
---
### Expansion de la menace : Le groupe Mustang Panda déploie une nouvelle variante de LOTUSLITE

Le groupe cybercriminel chinois Mustang Panda intensifie ses campagnes d'espionnage en utilisant une version évoluée du logiciel malveillant **LOTUSLITE**. Initialement axé sur des cibles gouvernementales américaines, le groupe diversifie désormais ses opérations vers le secteur bancaire indien et les cercles diplomatiques sud-coréens.

**Points clés :**
*   **Objectif :** Espionnage stratégique et politique plutôt que gain financier direct.
*   **Vecteur d'attaque :** Utilisation de fichiers d'aide compilés (CHM) piégés, contenant des leurres liés au secteur bancaire (ex: HDFC Bank) ou usurpant l'identité de personnalités diplomatiques.
*   **Fonctionnalités :** Le backdoor permet l'exécution de commandes à distance, la manipulation de fichiers et la gestion de sessions via HTTPS avec des serveurs de commande et de contrôle (C2).
*   **Technique de persistance :** Utilisation du **DLL side-loading** pour exécuter le malware (`dnx.onecore.dll`) à partir d'exécutables légitimes.

**Vulnérabilités :**
L'attaque repose sur le détournement de fonctionnalités légitimes de Windows (CHM et chargement de bibliothèques DLL) plutôt que sur l'exploitation d'une faille CVE spécifique. L'utilisation du format `.chm` permet de contourner certaines mesures de sécurité basiques en incitant l'utilisateur à interagir avec un contenu malveillant.

**Recommandations :**
*   **Sensibilisation :** Former les employés à la méfiance envers les pièces jointes de type `.chm` ou les documents sollicitant une interaction ("Oui/Non") inhabituelle.
*   **Filtrage réseau :** Bloquer les connexions sortantes vers les domaines suspects identifiés comme C2 (ex: `editor.gleeze[.]com` et `cosmosmusic[.]com`).
*   **Durcissement (Hardening) :** Restreindre l'exécution des fichiers CHM via des politiques de groupe (GPO) si leur utilisation n'est pas métier.
*   **Surveillance EDR :** Déployer des solutions de détection pour identifier les comportements anormaux liés au *DLL side-loading* et aux exécutions suspectes de processus hérités (tels que `hh.exe` pour les fichiers CHM).

---
[Source](https://thehackernews.com/2026/04/mustang-pandas-new-lotuslite-variant.html){:target="_blank"}
