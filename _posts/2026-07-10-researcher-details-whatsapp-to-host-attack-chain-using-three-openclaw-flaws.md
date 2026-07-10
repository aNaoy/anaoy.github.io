---
title: 'Researcher Details WhatsApp-to-Host Attack Chain Using Three OpenClaw Flaws'
date: 2026-07-10
permalink: /posts/2026/07/10/researcher-details-whatsapp-to-host-attack-chain-using-three-openclaw-flaws/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans OpenClaw : Risque d'exécution de code à distance via WhatsApp

Des chercheurs ont identifié trois vulnérabilités critiques dans l'assistant IA OpenClaw permettant une exécution de code arbitraire, une élévation de privilèges et le vol d'identifiants. Contrairement aux failles précédentes, ces vulnérabilités permettent une exploitation directe via l'envoi d'un simple message WhatsApp, sans nécessité de compromission préalable.

**Points clés :**
*   **Vecteur d'attaque :** Un attaquant peut déclencher l'exécution de code sur l'hôte en envoyant un message malveillant à l'agent IA via WhatsApp.
*   **Contournement de bac à sable (Sandbox) :** Les failles permettent de contourner les restrictions de montage de répertoires, donnant accès à des données sensibles (clés SSH, identifiants AWS, secrets GPG) ou au socket Docker, facilitant ainsi une évasion complète du conteneur.

**Vulnérabilités identifiées :**
*   **GHSA-hjr6-g723-hmfm (CVSS 8.8) :** Injection de commandes OS due à un filtrage insuffisant des entrées.
*   **GHSA-9969-8g9h-rxwm (CVSS 8.8) :** Injection de commandes OS similaire à la précédente, permettant d'exécuter des actions non autorisées.
*   **GHSA-575v-8hfq-m3mc (CVSS 8.4) :** Traversée de répertoire (Path Traversal) permettant de contourner les listes d'exclusion de montage et d'accéder à des répertoires système critiques.

**Recommandations :**
*   **Mise à jour immédiate :** Passer à la version **OpenClaw 2026.6.6** ou supérieure.
*   **Durcissement de la configuration :**
    *   Activer le mode « sandbox » pour toutes les sessions non principales.
    *   Retirer l'autorisation « exec » des outils utilisés par les agents exposés sur des canaux externes.
    *   Restreindre les listes d'autorisation aux opérateurs de confiance et désactiver les fonctionnalités inutilisées.
*   **Surveillance :** Inspecter les journaux pour détecter des commandes `git clone` utilisant le protocole `ext::`, souvent détourné pour l'exécution de commandes système arbitraires.

---
[Source](https://thehackernews.com/2026/07/researcher-details-whatsapp-to-host.html){:target="_blank"}
