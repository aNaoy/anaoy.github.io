---
title: 'Bitwarden CLI Compromised in Ongoing Checkmarx Supply Chain Campaign'
date: 2026-04-23
permalink: /posts/2026/04/23/bitwarden-cli-compromised-in-ongoing-checkmarx-supply-chain-campaign/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne d'approvisionnement de Bitwarden CLI

Une version malveillante de l'outil en ligne de commande de Bitwarden (`@bitwarden/cli@2026.4.0`) a été brièvement distribuée via npm le 22 avril 2026. Cette attaque s'inscrit dans une campagne plus large ciblant les développeurs et leurs environnements CI/CD.

**Points clés :**
*   **Vecteur d'attaque :** Compromission d'une action GitHub (GitHub Action) dans le pipeline CI/CD de Bitwarden, permettant de publier une version corrompue du paquet via le mécanisme de publication de confiance de npm.
*   **Objectif :** Exfiltration massive de secrets (tokens GitHub/npm, clés SSH, fichiers `.env`, historique shell) et compromission persistante des pipelines CI/CD des développeurs impactés.
*   **Propagation :** Les données volées étaient chiffrées (AES-256-GCM) et envoyées vers un domaine usurpant l'identité de Checkmarx ou via des commits GitHub.
*   **Impact :** Aucun risque pour les données des coffres-forts des utilisateurs finaux, selon Bitwarden. Seule la version spécifique `@bitwarden/cli@2026.4.0` était corrompue.
*   **Signatures :** L'attaque semble liée à la campagne "Shai-Hulud". Le malware inclut une condition d'arrêt automatique si la localisation du système cible est en Russie.

**Vulnérabilités :**
*   **Identifiant :** Une CVE est en cours d'attribution pour le paquet `@bitwarden/cli@2026.4.0`.

**Recommandations :**
*   **Vérification :** Les développeurs ayant installé la version `2026.4.0` du CLI Bitwarden durant la fenêtre de compromission (22 avril 2026, entre 17h57 et 19h30 ET) doivent considérer leurs secrets locaux, leurs tokens GitHub et leurs accès CI/CD comme compromis.
*   **Rotation des secrets :** Effectuer une rotation immédiate de tous les tokens et clés d'accès qui auraient pu être présents sur les machines où ce paquet a été installé.
*   **Audit de sécurité :** Vérifier les pipelines GitHub Actions à la recherche de workflows suspects ou d'injections malveillantes.
*   **Mise à jour :** S'assurer d'utiliser uniquement les versions légitimes et vérifiées du CLI Bitwarden après avoir réinitialisé les environnements de développement potentiellement exposés.

---
[Source](https://thehackernews.com/2026/04/bitwarden-cli-compromised-in-ongoing.html){:target="_blank"}
