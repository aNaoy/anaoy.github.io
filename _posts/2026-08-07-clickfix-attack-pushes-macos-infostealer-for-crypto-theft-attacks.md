---
title: 'ClickFix attack pushes macOS infostealer for crypto theft attacks'
date: 2026-08-07
permalink: /posts/2026/08/07/clickfix-attack-pushes-macos-infostealer-for-crypto-theft-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Propagation de malwares infostealers via des attaques « ClickFix » sur macOS

Une nouvelle campagne de malware basée sur le langage Go cible les utilisateurs de macOS. Cette menace utilise la technique « ClickFix » — qui consiste à inciter les victimes à exécuter des commandes dans le Terminal pour corriger de prétendues erreurs — afin d'installer un infostealer capable de dérober des actifs cryptographiques, des mots de passe enregistrés dans les navigateurs, des données du trousseau Apple (Keychain) et des cookies de session.

**Points clés :**
*   **Mode opératoire :** L'attaque commence par un email contenant un lien redirigeant vers une page Web. Celle-ci pousse la victime à copier-coller une commande dans le Terminal, téléchargeant un script Bash qui installe le payload malveillant.
*   **Persistance et évasion :** Le malware se dissimule dans un répertoire nommé `trustd` et utilise la commande `xattr -d com.apple.quarantine` pour contourner les protections de Gatekeeper. Il obtient des privilèges élevés via de fausses boîtes de dialogue système utilisant `osascript`.
*   **Vol sélectif :** Contrairement aux "drainers" classiques, ce malware peut calculer la valeur totale d'un portefeuille et ne dérober qu'un pourcentage défini des fonds, rendant le vol moins immédiatement détectable. Il cible diverses cryptomonnaies (Bitcoin, Ethereum, Monero, etc.).
*   **Infrastructure :** Le malware communique avec des serveurs situés au sein de l'Autonomous System 210644 (Aeza Group), un fournisseur de services d'hébergement "bulletproof" déjà sanctionné par les États-Unis et le Royaume-Uni.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée, car l'attaque repose sur l'ingénierie sociale (tromper l'utilisateur pour qu'il exécute manuellement du code malveillant) et l'abus de fonctionnalités système légitimes.

**Recommandations :**
*   **Sensibilisation :** Ne jamais copier-coller ou exécuter des commandes Terminal provenant de sites web ou d'emails non sollicités, même si l'interface promet de corriger une erreur système.
*   **Vigilance sur les privilèges :** Se méfier des boîtes de dialogue demandant un mot de passe administrateur qui apparaissent de manière inattendue ou inhabituelle.
*   **Sécurité des terminaux :** Utiliser des solutions EDR (Endpoint Detection and Response) capables de détecter les comportements anormaux, comme la modification suspecte d'attributs de fichiers ou l'exécution de scripts non autorisés dans le Terminal.
*   **Gestion des accès :** Utiliser un gestionnaire de mots de passe robuste et sécuriser les portefeuilles de cryptomonnaies avec une authentification matérielle (clé physique) plutôt que de stocker les clés privées directement dans le trousseau système ou les navigateurs.

---
[Source](https://www.bleepingcomputer.com/news/security/clickfix-attack-pushes-macos-infostealer-for-crypto-theft-attacks/){:target="_blank"}
