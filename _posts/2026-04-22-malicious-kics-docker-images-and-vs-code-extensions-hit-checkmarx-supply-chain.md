---
title: 'Malicious KICS Docker Images and VS Code Extensions Hit Checkmarx Supply Chain'
date: 2026-04-22
permalink: /posts/2026/04/22/malicious-kics-docker-images-and-vs-code-extensions-hit-checkmarx-supply-chain/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne d'approvisionnement logicielle de Checkmarx

Des attaquants ont compromis plusieurs canaux de distribution de l'outil KICS (Keeping Infrastructure as Code Secure) de Checkmarx, notamment le dépôt Docker Hub officiel et des extensions Visual Studio Code. Des versions malveillantes ont été injectées, permettant le vol de données sensibles contenues dans les fichiers d'infrastructure scannés.

**Points clés :**
*   **Docker Hub :** Des attaquants ont remplacé des tags officiels (`v2.1.20`, `alpine`) par des versions vérolées et ont ajouté une version non officielle (`v2.1.21`). Ces images contenaient un binaire KICS modifié capable de collecter, chiffrer et exfiltrer des rapports d'analyse vers un serveur distant.
*   **Extensions VS Code :** Les versions `1.17.0` et `1.19.0` de l'extension contenaient du code malveillant téléchargeant et exécutant des scripts JavaScript tiers via l'environnement Bun, sans vérification d'intégrité.
*   **Risque majeur :** La compromission expose potentiellement tous les secrets, identifiants et configurations sensibles ayant été scannés par ces versions corrompues.

**Vulnérabilités :**
*   Aucune CVE n'est associée à cet incident, car il s'agit d'une attaque par injection de code malveillant direct au sein de la chaîne d'approvisionnement (supply chain attack) plutôt que d'une faille logicielle classique.

**Recommandations :**
*   **Rotation des secrets :** Considérer comme compromis tout identifiant ou secret traité par les versions affectées de KICS. Procéder à une révocation et un renouvellement immédiats.
*   **Audit des systèmes :** Vérifier les logs d'exécution des outils de scan et des environnements de développement pour détecter des connexions vers des endpoints inconnus.
*   **Mise à jour :** S'assurer d'utiliser uniquement les versions officielles et intègres des outils, en privilégiant les sources de confiance et en vérifiant les sommes de contrôle si disponibles.
*   **Veille :** Surveiller les communications officielles de Checkmarx concernant le rétablissement de la sécurité de leurs dépôts et extensions.

---
[Source](https://thehackernews.com/2026/04/malicious-kics-docker-images-and-vs.html){:target="_blank"}
