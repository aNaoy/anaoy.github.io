---
title: 'ReVault! When your SoC turns against you…'
date: 2025-08-06
permalink: /posts/2025/08/06/revault-when-your-soc-turns-against-you/
tags:
- veille-cyber
- zerodaysfans
---
## ReVault : Des vulnérabilités dans le système de sécurité matériel de Dell

Des vulnérabilités ont été découvertes dans le firmware ControlVault3 (CV) et ses API Windows associées de Dell, baptisées "ReVault". Ces failles affectent plus de 100 modèles d'ordinateurs portables Dell et peuvent permettre la persistance d'un attaquant même après une réinstallation de Windows, ainsi que le contournement de la connexion Windows ou l'obtention de privilèges administrateur via une attaque physique.

Le ControlVault est une solution de sécurité matérielle conçue pour stocker de manière sécurisée des mots de passe, des données biométriques et des codes de sécurité dans le firmware. Il est implémenté sur une carte fille appelée Unified Security Hub (USH), qui sert de concentrateur pour les périphériques de sécurité tels que les lecteurs d'empreintes digitales, de cartes à puce et de NFC. Les versions ControlVault3 et ControlVault3+ sont présentes dans des modèles couramment utilisés dans des environnements sensibles comme la cybersécurité et les secteurs gouvernementaux.

**Points Clés et Vulnérabilités :**

*   **Type de vulnérabilités :** Cinq vulnérabilités ont été identifiées dans le firmware CV, incluant des dépassements de tampon (out-of-bounds) et des débordements de pile (stack-overflow). Une sixième vulnérabilité d'unsafe-deserialization affecte les API Windows de ControlVault.
*   **Impact des vulnérabilités :**
    *   **Persistance post-compromission :** Un utilisateur sans privilèges peut déclencher une exécution de code arbitraire sur le firmware CV via les API Windows. Cela peut permettre de voler des clés de chiffrement et de modifier le firmware de manière permanente, créant un implant résistant aux réinstallations du système d'exploitation.
    *   **Attaque physique :** Un attaquant avec un accès physique à l'ordinateur peut accéder directement à la carte USH via USB. Cela lui permet d'exploiter les vulnérabilités sans avoir à se connecter au système ni connaître les mots de passe. Il est possible de modifier le firmware pour accepter n'importe quelle empreinte digitale pour le déverrouillage.
*   **CVE identifiées :**
    *   CVE-2025-24311 (dépassement de tampon)
    *   CVE-2025-25050 (dépassement de tampon)
    *   CVE-2025-25215 (arbitrary free)
    *   CVE-2025-24922 (stack-overflow)
    *   CVE-2025-24919 (unsafe-deserialization)

**Recommandations :**

*   **Mises à jour :** Maintenir le système à jour pour installer le dernier firmware ControlVault, qui peut être déployé via Windows Update ou directement depuis le site de Dell.
*   **Désactivation des services :** Si les périphériques de sécurité (lecteur d'empreintes digitales, lecteur de carte à puce, lecteur NFC) ne sont pas utilisés, il est possible de désactiver les services ControlVault via le gestionnaire de services ou le périphérique lui-même via le gestionnaire de périphériques.
*   **Désactivation de la connexion par empreinte digitale :** Envisager de désactiver la connexion par empreinte digitale lorsque le risque est élevé (par exemple, laisser l'ordinateur portable sans surveillance). L'utilisation de la fonction "Enhanced Sign-in Security" (ESS) de Windows peut également aider à atténuer certaines attaques physiques et à détecter un firmware CV compromis.

**Détection :**

*   **Chassis Intrusion Detection :** Activer la détection d'intrusion du châssis dans le BIOS, si disponible, pour signaler toute manipulation physique.
*   **Journaux Windows :** Surveiller les plantages inattendus du service biométrique Windows ou des services Credential Vault, qui pourraient indiquer une compromission.
*   **Outils de sécurité :** Les solutions comme Cisco Secure Endpoint peuvent détecter des activités suspectes avec des signatures spécifiques, comme "bcmbipdll.dll Loaded by Abnormal Process".

Ces découvertes soulignent la nécessité d'évaluer la posture de sécurité de tous les composants matériels d'un appareil, et pas seulement du système d'exploitation. Une vigilance constante, la mise à jour des systèmes et l'évaluation proactive des risques sont essentielles pour se protéger contre les menaces évolutives.
---
Source: https://blog.talosintelligence.com/revault-when-your-soc-turns-against-you/
