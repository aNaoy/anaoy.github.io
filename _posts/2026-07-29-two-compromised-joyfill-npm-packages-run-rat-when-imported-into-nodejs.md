---
title: 'Two Compromised joyfill npm Packages Run RAT When Imported Into Node.js'
date: 2026-07-29
permalink: /posts/2026/07/29/two-compromised-joyfill-npm-packages-run-rat-when-imported-into-nodejs/
tags:
- veille-cyber
- hackernews
---
### Compromission de paquets npm : Propagation du malware DEV#POPPER

Des versions bêta de deux paquets de la bibliothèque `@joyfill` ont été compromises pour infecter les environnements Node.js avec un cheval de Troie d'accès à distance (RAT). Attribuée à des acteurs liés à la Corée du Nord, cette attaque utilise une infrastructure de commande et contrôle (C2) basée sur la blockchain pour contourner les méthodes de détection classiques.

**Points clés :**
*   **Vecteur d'infection :** Contrairement aux malwares déclenchés par des hooks npm, le code malveillant s'exécute dès l'importation du paquet (CommonJS) dans Node.js.
*   **Infrastructure résiliente :** Le malware interroge des transactions sur les blockchains Tron, Aptos et BNB Smart Chain pour récupérer dynamiquement ses instructions, rendant le contrôle des charges utiles plus flexible et furtif.
*   **Double mécanisme :** L'implant utilise une exécution en mémoire et un processus Node.js détaché (persistant après la fermeture des tâches de build) pour charger le RAT `clientCode` et un voleur d'informations (stealer) de type OmniStealer.
*   **Capacités :** Exfiltration de fichiers, vol de données d'identification (navigateurs, Git, VS Code, gestionnaires de mots de passe), lecture du presse-papiers et exécution de commandes arbitraires.
*   **Évasion :** Le malware détecte et évite l'exécution sur les environnements CI/CD connus (GitHub Runners, Buildbot, etc.) pour limiter son exposition aux chercheurs en sécurité.

**Paquets affectés :**
*   `@joyfill/layouts@0.1.2-2773.beta.0`
*   `@joyfill/components@4.0.0-rc24-2773-beta.4`

**Vulnérabilités :**
Aucune CVE spécifique n'a été attribuée, car il s'agit d'une attaque par injection de code malveillant dans la chaîne d'approvisionnement logicielle (*Supply Chain Attack*).

**Recommandations :**
*   **Suppression immédiate :** Supprimer les versions compromises des `lockfiles`, caches npm, miroirs internes, images de build et artefacts de déploiement.
*   **Nettoyage :** Revenir à une version vérifiée et sécurisée du paquet.
*   **Rotation des secrets :** Considérer comme compromis tous les identifiants, jetons d'accès et clés API présents sur les machines où ces versions ont été exécutées, et procéder à leur renouvellement immédiat.
*   **Audit :** Vérifier les logs des environnements de développement et de CI/CD à la recherche d'activités suspectes ou de connexions sortantes vers des adresses IP/blockchain inconnues.

---
[Source](https://thehackernews.com/2026/07/two-compromised-joyfill-npm-packages.html){:target="_blank"}
