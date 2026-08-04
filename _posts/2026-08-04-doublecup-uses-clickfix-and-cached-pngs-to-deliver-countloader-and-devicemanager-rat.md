---
title: 'DOUBLECUP Uses ClickFix and Cached PNGs to Deliver CountLoader and DeviceManager RAT'
date: 2026-08-04
permalink: /posts/2026/08/04/doublecup-uses-clickfix-and-cached-pngs-to-deliver-countloader-and-devicemanager-rat/
tags:
- veille-cyber
- hackernews
---
### DOUBLECUP : Analyse d'une nouvelle plateforme de distribution de malwares

**DOUBLECUP** est un service de type *Loader-as-a-Service* (LaaS) actif depuis juin 2026, spécialisé dans la distribution de malwares via des attaques de type **ClickFix**. Le service permet à des opérateurs de créer des campagnes malveillantes utilisant des leurres (pages de connexion CRM usurpées) pour injecter des scripts malveillants par le biais du presse-papier de la victime.

**Points clés :**
*   **Méthode de livraison :** Utilisation de la stéganographie (images PNG cachées dans le cache du navigateur) et de techniques d'ingénierie sociale ClickFix pour exécuter des payloads.
*   **Techniques d'évasion :** Le payload final est déchiffré en mémoire en utilisant l'adresse IP publique de la victime comme clé de chiffrement (*environmental keying*).
*   **Malwares distribués :**
    *   **CountLoader :** Un loader capable de persister sur Windows et macOS, capable d'exfiltrer des données et d'exécuter des binaires distants.
    *   **DeviceManager :** Un RAT (Remote Access Trojan) modulaire en Python utilisant la technique **EtherHiding** (résolution des serveurs C2 via des contrats intelligents sur les blockchains Ethereum/Polygon).
*   **Ciblage :** Les deux malwares évitent les systèmes localisés dans les pays de la Communauté des États indépendants (CEI).

**Vulnérabilités :**
L'article ne mentionne pas de CVE spécifique exploitée, car il s'agit d'une campagne basée sur l'ingénierie sociale (ClickFix) et l'exécution de code légitime détourné. La faille repose principalement sur l'interaction de l'utilisateur avec des interfaces trompeuses qui incitent à exécuter manuellement des commandes dans le terminal.

**Recommandations :**
*   **Sensibilisation :** Informer les utilisateurs des dangers liés aux instructions "ClickFix" (copier-coller des commandes dans le terminal ou le menu Exécuter de Windows).
*   **Filtrage réseau :** Surveiller et bloquer les communications vers des infrastructures utilisant des techniques de *DNS Tunneling* et les requêtes suspectes vers des contrats intelligents de blockchain.
*   **Contrôle des endpoints :**
    *   Limiter l'exécution de scripts PowerShell et VBScript via des politiques de restriction logicielle (AppLocker/WDAC).
    *   Utiliser des solutions EDR capables de détecter le comportement de chargement de payloads en mémoire et les tentatives de modification de raccourcis (.LNK).
*   **Validation des extensions :** Se méfier des extensions tierces (ex: "Agent IDE" sur VS Code) associées à des identités suspectes identifiées par les chercheurs en sécurité.

---
[Source](https://thehackernews.com/2026/08/doublecup-uses-clickfix-and-cached-pngs.html){:target="_blank"}
