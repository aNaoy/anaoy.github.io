---
title: 'New OkoBot framework deploys 20 payloads to steal data, crypto'
date: 2026-07-17
permalink: /posts/2026/07/17/new-okobot-framework-deploys-20-payloads-to-steal-data-crypto/
tags:
- veille-cyber
- bleepingcomp
---
### OkoBot : un framework malveillant sophistiqué dédié au vol de données et de cryptomonnaies

OkoBot est un framework malveillant actif depuis début 2026, évoluant à partir de la campagne TookPS. Il déploie plus de 20 charges utiles pour exfiltrer des identifiants, des cookies et des phrases de récupération (seed phrases) de portefeuilles de cryptomonnaies.

**Points clés :**
*   **Vecteurs d'infection :** Attaques par "ClickFix" et dépôts GitHub frauduleux (logiciels légitimes trojanisés).
*   **Fonctionnement :** Utilisation d'un bot SSH pour la collecte initiale d'informations système et la désactivation des alertes Windows Defender.
*   **Ciblage :** Portefeuilles matériels (Trezor, Ledger), navigateurs (Chrome), gestionnaires de mots de passe et applications financières.
*   **Origine probable :** Des indices (commentaires dans le code source, forums spécialisés) suggèrent un acteur russophone, avec une géolocalisation interdisant l'infection vers la Russie et les pays de la CEI.

**Composants malveillants majeurs :**
*   **Injecteurs de navigateurs :** Installation silencieuse d'extensions comme *Rilide* pour le vol de données financières.
*   **SeedHunter :** Injection dans les logiciels de portefeuilles pour afficher de faux écrans de récupération.
*   **MC Keylogger :** Enregistrement des frappes clavier, du presse-papier, des connexions USB et captures d'écran.
*   **OkoSpyware :** Surveillance vidéo et capture de données sur plus de 100 programmes spécifiques.

**Vulnérabilités :**
Aucune CVE spécifique n'est mentionnée, car OkoBot repose sur l'ingénierie sociale, l'exécution de scripts PowerShell malveillants et l'injection de code dans des processus légitimes pour contourner les protections.

**Recommandations :**
*   **Vérification des sources :** Ne télécharger des logiciels que depuis les sites officiels des éditeurs et éviter les dépôts GitHub non vérifiés.
*   **Sensibilisation :** Se méfier des sites demandant de cliquer sur des boutons de "correction" ou de mise à jour (ClickFix).
*   **Sécurité des actifs :** Ne jamais saisir de phrase de récupération (seed phrase) en dehors de l'interface physique sécurisée du portefeuille matériel.
*   **Surveillance :** Utiliser des indicateurs de compromission (IOC) fournis par les rapports de cybersécurité (tels que ceux de Kaspersky) pour auditer les réseaux et les terminaux.
*   **Protection endpoint :** Maintenir les solutions EDR/AV à jour et surveiller les processus suspects injectant du code dans les navigateurs.

---
[Source](https://www.bleepingcomputer.com/news/security/new-okobot-framework-deploys-20-payloads-to-steal-data-crypto/){:target="_blank"}
