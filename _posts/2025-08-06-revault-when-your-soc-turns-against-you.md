
---
title: 'ReVault! When your SoC turns against you…'
date: 2025-08-06
permalink: /posts/2025/08/06/revault-when-your-soc-turns-against-you/
tags:
- veille-cyber
- zerodaysfans
---
### Compromission du ControlVault Dell : Persistance et Contournement d'Authentification

Des vulnérabilités critiques ont été découvertes dans le firmware du Dell ControlVault3 (CV) et ses API Windows associées, baptisées "ReVault". Ces failles affectent plus de 100 modèles d'ordinateurs portables Dell, si elles ne sont pas corrigées. L'exploitation de ces failles permet à des attaquants de maintenir une présence persistante sur un système, même après une réinstallation de Windows, ou de contourner l'authentification Windows et d'obtenir des privilèges administrateur localement.

Le Dell ControlVault est une solution de sécurité matérielle qui sécurise des informations sensibles comme les mots de passe et les données biométriques dans le firmware, hébergé sur une carte dédiée appelée Unified Security Hub (USH). Ces vulnérabilités touchent des appareils couramment utilisés dans des secteurs sensibles tels que la cybersécurité et les environnements gouvernementaux.

**Points Clés et Vulnérabilités Découvertes :**

*   **Cinq vulnérabilités** ont été signalées, affectant le firmware CV et les API Windows :
    *   Plusieurs dépassements de tampon (out-of-bounds): CVE-2025-24311, CVE-2025-25050
    *   Libération arbitraire de mémoire (arbitrary free): CVE-2025-25215
    *   Dépassement de pile (stack-overflow): CVE-2025-24922
    *   Désérialisation non sécurisée (unsafe-deserialization) affectant les API Windows : CVE-2025-24919

*   **Scénarios d'Attaque Majeurs :**
    *   **Pivot post-compromission :** Un utilisateur non-administrateur peut exécuter du code arbitraire sur le firmware CV, permettant de voler des clés de chiffrement et de modifier le firmware de manière permanente. Un implant pourrait ainsi persister sur la durée et être réutilisé par un attaquant.
    *   **Attaque physique :** Un attaquant ayant un accès physique peut accéder à la carte USH via USB. Il peut alors exploiter les vulnérabilités sans avoir besoin de se connecter au système ou de connaître les mots de passe. Il est même possible de modifier le firmware pour accepter n'importe quelle empreinte digitale pour le déverrouillage.

**Recommandations :**

*   **Maintenir les systèmes à jour :** Installer les dernières mises à jour du firmware du ControlVault.
*   **Désactiver les services si inutilisés :** Si les périphériques de sécurité comme le lecteur d'empreintes digitales ne sont pas utilisés, il est recommandé de désactiver les services CV via le Gestionnaire de Services et/ou l'appareil CV via le Gestionnaire de Périphériques.
*   **Désactiver l'authentification par empreinte digitale :** Envisager de désactiver cette option dans les environnements à risque accru.
*   **Activer la Sécurité de Connexion Améliorée (ESS) :** Sous Windows, l'ESS peut aider à atténuer certaines attaques physiques et à détecter une modification anormale du firmware CV.

**Détection :**

*   Activer la détection d'intrusion du châssis dans le BIOS.
*   Surveiller les journaux Windows pour des plantages inattendus des services biométriques ou de gestion des identifiants.
*   Les solutions de sécurité comme Cisco Secure Endpoint peuvent détecter des comportements suspects liés aux fichiers du ControlVault.
---
Source: https://blog.talosintelligence.com/revault-when-your-soc-turns-against-you/
