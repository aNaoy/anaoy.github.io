---
title: 'China-Aligned Bronze Sandcastle Abuses Sandboxie DLL Sideloading to Deploy Backdoors'
date: 2026-10-21
permalink: /posts/2026/10/21/china-aligned-bronze-sandcastle-abuses-sandboxie-dll-sideloading-to-deploy-backdoors/
tags:
- veille-cyber
- hackernews
---
### Menace persistante : Le groupe Bronze Sandcastle et l'exploitation du DLL Sideloading

Le groupe cybercriminel affilié à la Chine, baptisé **Bronze Sandcastle**, cible des organisations en Asie et en Afrique depuis mi-2025. Ce groupe se distingue par l'utilisation systématique du *DLL sideloading* pour déployer des portes dérobées (backdoors) tout en échappant aux solutions de détection classiques.

**Points clés :**
*   **Technique principale :** Détournement de chargement de DLL (*DLL Sideloading*), principalement via des versions légitimes de l'utilitaire **Sandboxie** (exécutable `SandboxieWUAU.exe` associé à la DLL malveillante `sbiedll.dll`).
*   **Diversification :** Le groupe utilise également sept autres combinaisons d'exécutables légitimes (dont Java, Krita, NVDA, Sysinternals) pour masquer ses activités.
*   **Fonctionnement :** Une fois chargée, la DLL malveillante déchiffre et exécute un fichier de configuration (`config.ini`) en mémoire. Cela permet au groupe d'exécuter des commandes, de voler des données système, d'enregistrer les frappes clavier et de réaliser des captures d'écran.
*   **Infrastructure C2 :** Communication avec des services tiers (GitHub, file.io, Ably) ou des domaines imitant des entités légitimes pour masquer le trafic de commande et contrôle.

**Vulnérabilités :**
Il ne s'agit pas de failles logicielles classiques (CVE), mais de l'exploitation de la **conception du processus de recherche des DLL sous Windows** (référencé sous le code MITRE **T1574.001**). Lorsqu'une application ne spécifie pas le chemin complet d'une dépendance, Windows recherche celle-ci dans des répertoires locaux potentiellement accessibles par l'attaquant.

**Recommandations :**
*   **Surveillance comportementale :** Privilégier la détection des comportements suspects plutôt que la recherche de signatures statiques (fichiers malveillants), car le code est souvent exécuté en mémoire.
*   **Analyse des accès fichiers :** Surveiller les processus signés et légitimes qui accèdent de manière inhabituelle à des fichiers de configuration ou des bibliothèques situées dans des répertoires locaux.
*   **Limitation des privilèges :** Restreindre les droits d'écriture dans les dossiers d'installation des applications pour empêcher l'insertion de DLL malveillantes.
*   **Audit des processus :** Identifier et surveiller l'exécution récurrente de binaires connus utilisés pour le sideloading (ex: `SandboxieWUAU.exe`, `bginfo64.exe`) au sein de l'environnement de travail.

---
[Source](https://thehackernews.com/2026/10/china-aligned-bronze-sandcastle-abuses.html){:target="_blank"}
