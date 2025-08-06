---
title: 'ReVault! When your SoC turns against you…'
date: 2025-08-06
permalink: /posts/2025/08/06/revault-when-your-soc-turns-against-you/
tags:
- veille-cyber
- zerodaysfans
---
**ReVault : Menaces sur la Sécurité Matérielle des Ordinateurs Portables Dell**

Des chercheurs ont découvert une série de vulnérabilités, baptisées "ReVault", affectant le firmware ControlVault3 et ses API Windows sur plus de 100 modèles d'ordinateurs portables Dell. Ces failles peuvent permettre à des attaquants de maintenir une présence sur le système même après une réinstallation de Windows, de contourner les connexions Windows, ou d'obtenir des privilèges d'administrateur locaux.

Le Dell ControlVault est une solution de sécurité matérielle intégrée dans une carte fille dédiée (Unified Security Hub - USH) qui gère les données sensibles comme les mots de passe et les informations biométriques.

**Points Clés :**

*   **Impact généralisé :** Plus de 100 modèles de portables Dell sont concernés.
*   **Persistance avancée :** Une fois exploitée, l'attaque peut persister même après une réinstallation complète du système d'exploitation.
*   **Contournement d'authentification :** Permet de contourner la connexion Windows et les authentifications biométriques (comme l'empreinte digitale).
*   **Escalade de privilèges :** Un attaquant local peut obtenir des droits d'administrateur.

**Vulnérabilités identifiées (CVE) :**

*   **Firmware ControlVault3 :**
    *   CVE-2025-24311 (Dépassement de tampon)
    *   CVE-2025-25050 (Dépassement de tampon)
    *   CVE-2025-25215 (Libération arbitraire)
    *   CVE-2025-24922 (Dépassement de pile)
*   **API Windows ControlVault :**
    *   CVE-2025-24919 (Désérialisation non sécurisée)

**Scénarios d'attaque :**

1.  **Post-compromission et Persistance :** Un utilisateur sans privilèges peut exploiter les API ControlVault pour exécuter du code arbitraire sur le firmware, voler des clés de chiffrement et modifier le firmware de manière permanente. Cela permet de créer un implant indétectable qui peut être utilisé pour reprendre le contrôle du système ultérieurement.
2.  **Attaque Physique :** Un attaquant ayant un accès physique à l'ordinateur peut ouvrir le châssis, accéder directement à la carte USH via USB et exploiter les vulnérabilités sans avoir à se connecter au système. Il est même possible de modifier le firmware pour accepter n'importe quelle empreinte digitale pour le déverrouillage.

**Recommandations :**

*   **Maintenir le système à jour :** Installer les dernières mises à jour du firmware ControlVault. Celles-ci peuvent être déployées via Windows Update ou directement sur le site de Dell.
*   **Désactiver les services non utilisés :** Si les périphériques de sécurité (lecteur d'empreintes, lecteur de carte à puce, NFC) ne sont pas utilisés, il est possible de désactiver les services et le périphérique ControlVault via le Gestionnaire de services ou le Gestionnaire de périphériques.
*   **Gérer la sécurité de la connexion :** Désactiver la connexion par empreinte digitale dans les situations à risque. Activer la fonctionnalité "Enhanced Sign-in Security" (ESS) de Windows peut aider à atténuer certaines attaques physiques et détecter des modifications du firmware.

**Détection :**

*   **Intrusion du châssis :** Activer la détection d'intrusion du châssis dans le BIOS pour signaler toute ouverture physique du boîtier.
*   **Anomalies dans les journaux Windows :** Surveiller les plantages inattendus des services biométriques ou des services de Credential Vault.
*   **Alertes de sécurité :** Les solutions comme Cisco Secure Endpoint peuvent émettre des alertes pour des comportements suspects liés aux composants du ControlVault.
---
[Source](https://blog.talosintelligence.com/revault-when-your-soc-turns-against-you/){:target="_blank"}
