---
title: 'Chinese-Speaking APT Deploys New TinyRCT Backdoor in Southeast Asia Campaign'
date: 2026-06-26
permalink: /posts/2026/06/26/chinese-speaking-apt-deploys-new-tinyrct-backdoor-in-southeast-asia-campaign/
tags:
- veille-cyber
- hackernews
---
### Menace persistante : Déploiement du backdoor TinyRCT en Asie du Sud-Est

Le groupe APT sinophone identifié sous le nom **CL-STA-1062** (lié à UAT-7237) mène une campagne prolongée contre des entités gouvernementales et des infrastructures critiques en Asie du Sud-Est. Les attaquants utilisent une approche hybride mêlant outils open source et malwares personnalisés pour infiltrer les réseaux, effectuer des mouvements latéraux et exfiltrer des données sensibles.

**Points clés :**
*   **Mode opératoire :** Utilisation de shells web (ASPX) pour l'accès initial, suivis d'une reconnaissance réseau et du déploiement de payloads.
*   **Outils hybrides :** Combinaison d'outils légitimes détournés (SoftEther VPN, Mimikatz, VNT, proxy SOCKS5 Yuze) et du nouveau backdoor **TinyRCT**.
*   **Technique d'injection :** TinyRCT est déployé via une attaque de type *AppDomainManager injection* (T1574.014), utilisant une DLL malveillante chargée par un exécutable légitime (Chrome).
*   **Ciblage :** Au moins 10 organisations visées entre octobre et décembre 2025, avec une préférence pour les secteurs de l'énergie et gouvernementaux.

**Vulnérabilités exploitées :**
*   Le vecteur principal repose sur l'exploitation de vulnérabilités non spécifiées sur les serveurs Web et serveurs MS SQL pour installer des web shells.
*   Utilisation de la technique d'injection **AppDomainManager** pour contourner les contrôles de sécurité et charger du code arbitraire.

**Capacités de TinyRCT :**
*   Exécution de commandes arbitraires et énumération de fichiers.
*   Capture d'écran et exfiltration de données.
*   Auto-suppression pour effacer les traces de l'infection.
*   Communication chiffrée (AES-128-CBC) avec un serveur C2 via des requêtes HTTP.
*   Mécanisme d'anti-sandbox pour éviter la détection dans les environnements de test.

**Recommandations :**
*   **Surveillance réseau :** Détecter les beacons HTTP suspects avec un intervalle régulier (défaut de 10 secondes) et surveiller les communications vers les adresses IP liées aux attaquants (ex: `45.32.113[.]172` et `139.180.134[.]221`).
*   **Gestion des logs :** Auditer les répertoires des serveurs web à la recherche de fichiers suspects (web shells) et surveiller les processus lancés sous des noms trompeurs (ex: `vmtools.exe`, `XDRAgent.exe`).
*   **Durcissement :** Restreindre l'utilisation des outils VPN et SOCKS5 non autorisés dans l'environnement.
*   **Analyse comportementale :** Surveiller les exécutions anormales utilisant `AppDomainManager` pour charger des DLL dans des applications apparemment légitimes.

---
[Source](https://thehackernews.com/2026/06/chinese-speaking-apt-deploys-new.html){:target="_blank"}
