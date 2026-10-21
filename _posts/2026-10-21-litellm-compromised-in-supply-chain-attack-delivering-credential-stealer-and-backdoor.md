---
title: 'LiteLLM Compromised in Supply Chain Attack Delivering Credential Stealer and Backdoor'
date: 2026-10-21
permalink: /posts/2026/10/21/litellm-compromised-in-supply-chain-attack-delivering-credential-stealer-and-backdoor/
tags:
- veille-cyber
- hackernews
---
### Attaque de la chaîne d'approvisionnement sur le paquet Python LiteLLM

Le paquet Python **LiteLLM** a été compromis dans sa version **1.107.0**, permettant l'injection d'un logiciel malveillant via des roues (wheels) PyPI et des images Docker. L'attaque a été facilitée par le vol de jetons OAuth GitHub appartenant à des ingénieurs du projet, permettant aux attaquants de signer et de publier la version compromise.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation de jetons GitHub CLI volés pour déclencher et approuver des déploiements malveillants.
*   **Mécanisme d'exécution :** Le malware utilise un fichier `cook.pth` qui force l'exécution automatique de code dès le démarrage de l'interpréteur Python, avant même l'importation de la bibliothèque.
*   **Capacités du malware :**
    *   **Vol de données :** Collecte de clés privées, jetons cloud, données de navigateurs (Chromium/Firefox), variables d'environnement et fichiers de configuration d'outils d'IA.
    *   **Backdoor :** Exécution d'un démon en arrière-plan capable de récupérer et d'exécuter du code distant depuis un dépôt GitHub (mécanisme de "dead drop").
    *   **Exfiltration :** Envoi des données collectées via une requête HTTP POST vers `litellm[.]dev/healthcheck`.

**Vulnérabilités :**
*   Aucun identifiant CVE spécifique n'a été attribué à ce jour, l'incident étant classé comme une compromission directe de la chaîne d'approvisionnement logicielle via des comptes mainteneurs compromis.

**Recommandations :**
*   **Réinitialisation immédiate :** Si la version 1.107.0 a été installée, considérez tous les jetons, clés API, mots de passe et fichiers de configuration présents sur la machine comme compromis. Révoquez et remplacez-les depuis un environnement propre.
*   **Contrôle de version :** Utilisez le verrouillage par empreinte (digest) pour forcer l'utilisation de la version sécurisée précédente (**1.106.2**).
*   **Audit de sécurité :** Appliquez le principe du moindre privilège aux jetons GitHub des développeurs et assurez-vous que l'approbation des publications repose sur des mécanismes d'authentification robuste (MFA).

---
[Source](https://thehackernews.com/2026/10/litellm-compromised-in-supply-chain.html){:target="_blank"}
