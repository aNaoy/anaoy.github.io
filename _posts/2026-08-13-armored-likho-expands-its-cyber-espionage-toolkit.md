---
title: 'Armored Likho expands its cyber-espionage toolkit'
date: 2026-08-13
permalink: /posts/2026/08/13/armored-likho-expands-its-cyber-espionage-toolkit/
tags:
- veille-cyber
- securelist
---
### Expansion de l'arsenal d'espionnage du groupe Armored Likho

Le groupe de cyber-espionnage **Armored Likho** (alias Eagle Werewolf) a intensifié ses activités en 2026, ciblant des organisations et particuliers en Russie. Cette campagne repose sur un nouveau kit d'outils développé en Rust, baptisé **Still Toolkit**, conçu pour l'exfiltration de données et la surveillance audio.

#### Points clés
*   **Vecteur d'infection :** Un "dropper" déguisé en application de dons caritatifs, développé via le framework Tauri, qui exécute la charge utile de manière dissimulée.
*   **Still Sync :** Un module capable de voler les sessions Telegram (dossier `tdata`) pour accéder aux discussions, fichiers médias et contacts via l'API Telegram.
*   **Still Audio :** Un implant de surveillance audio utilisant un algorithme VAD (Voice Activity Detection) pour détecter et enregistrer les conversations, puis les envoyer à un serveur de commande et contrôle (C2).
*   **Persistance et furtivité :** Utilisation de services Windows personnalisés (ex: `TReload`, `auxhost`) et de techniques de *Dead Drop Resolver* (via GitHub) pour maintenir la connexion au C2.
*   **Ciblage :** Secteurs public, privé, IT et éducation en Russie.

#### Vulnérabilités exploitées
Bien qu'aucune CVE spécifique ne soit mentionnée, les attaquants abusent de fonctionnalités légitimes du système :
*   **SeBackupPrivilege :** Exploitation de ces privilèges pour forcer la lecture de fichiers (notamment `tdata`) via le service Shadow Copy ou l'utilitaire `Robocopy`.
*   **Abus de services légitimes :** Utilisation de bibliothèques audio standard (encodage via `libmp3lame`) et création de services Windows masqués pour se fondre dans le trafic système.

#### Recommandations
*   **Surveillance des terminaux (EDR) :** Détecter l'exécution de processus suspects liés aux services `TReload` ou `auxhost`, ainsi que l'utilisation inhabituelle de `Robocopy` ou des accès au service Shadow Copy.
*   **Gestion des accès :** Protéger les dossiers contenant les données de session d'applications de messagerie (ex: `tdata` pour Telegram Desktop).
*   **Analyse des permissions :** Restreindre les privilèges `SeBackupPrivilege` aux seuls comptes administrateurs nécessaires.
*   **Hygiène numérique :** Sensibiliser les utilisateurs aux risques liés aux applications de "dons" non officielles et surveiller les applications ayant accès au microphone dans les paramètres de confidentialité de Windows.
*   **Indicateurs de compromission :** Bloquer les domaines associés (ex: `tg4service[.]com`, `srwinservice[.]com`, `orderapiserver[.]info`) et surveiller la présence des hashs des fichiers identifiés dans le rapport.

---
[Source](https://securelist.com/armored-likho-still-toolkit/121033/){:target="_blank"}
