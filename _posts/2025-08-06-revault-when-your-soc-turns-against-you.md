---
title: 'ReVault! When your SoC turns against you…'
date: 2025-08-06
permalink: /posts/2025/08/06/revault-when-your-soc-turns-against-you/
tags:
- veille-cyber
- zerodaysfans
---
**ReVault : Quand le système sur puce (SoC) se retourne contre vous**

Des vulnérabilités critiques ont été découvertes dans le firmware ControlVault3 et les API Windows associées de Dell, baptisées "ReVault". Affectant plus de 100 modèles d'ordinateurs portables Dell, ces failles peuvent être exploitées pour assurer une persistance après compromission, survivant même à des réinstallations de Windows. Elles permettent également de contourner la connexion Windows ou d'obtenir des privilèges administrateur avec un accès physique.

Le ControlVault (CV) est une solution de sécurité matérielle intégrée au firmware, gérant des données sensibles comme les mots de passe et les données biométriques via une carte fille appelée Unified Security Hub (USH). Les versions ControlVault3 et ControlVault3+ sont présentes dans de nombreux modèles professionnels de Dell (Latitude, Precision), utilisés dans des environnements sensibles nécessitant des authentifications renforcées.

**Points clés et vulnérabilités :**

*   **Cinq vulnérabilités majeures découvertes par Talos** :
    *   Plusieurs dépassements de tampon (CVE-2025-24311, CVE-2025-25050).
    *   Libération arbitraire (CVE-2025-25215).
    *   Dépassement de pile (CVE-2025-24922), affectant le firmware CV.
    *   Désérialisation non sécurisée (CVE-2025-24919), affectant les API Windows de ControlVault.

*   **Impacts critiques :**
    *   **Persistance post-compromission** : Un utilisateur sans privilèges peut déclencher une exécution de code arbitraire sur le firmware CV via les API. Cela permet de voler des clés de chiffrement, de modifier le firmware de manière permanente et d'établir un implant persistant qui peut être réutilisé pour accéder au système, même après une réinstallation de Windows.
    *   **Attaque physique** : Un attaquant avec un accès physique peut accéder directement à la carte USH via USB. Toutes les vulnérabilités deviennent exploitables sans avoir besoin de se connecter au système ou de connaître les mots de passe. Il est possible de modifier le firmware pour accepter n'importe quelle empreinte digitale pour déverrouiller le système.

**Recommandations :**

*   **Mises à jour** : Maintenir les systèmes à jour pour garantir l'installation du dernier firmware ControlVault. Les mises à jour peuvent être déployées via Windows Update ou directement depuis le site de Dell.
*   **Désactivation des services** : Si les périphériques de sécurité (lecteur d'empreintes digitales, carte à puce, NFC) ne sont pas utilisés, il est recommandé de désactiver les services ControlVault via le Gestionnaire de services ou le périphérique via le Gestionnaire de périphériques.
*   **Sécurité des connexions** : Envisager de désactiver la connexion par empreinte digitale dans les environnements à risque accru. L'activation de la sécurité renforcée de Windows (ESS) peut également aider à atténuer certaines attaques physiques et à détecter un firmware CV compromis.

**Détection :**

*   **Intrusion physique** : Activer la détection d'intrusion physique dans le BIOS de l'ordinateur portable peut signaler une manipulation matérielle.
*   **Journaux Windows** : Des plantages inattendus du service biométrique Windows ou des services Credential Vault peuvent indiquer une compromission.
*   **Solutions de sécurité** : Pour les clients utilisant Cisco Secure Endpoint, une signature spécifique ("bcmbipdll.dll Loaded by Abnormal Process") peut alerter sur des risques potentiels.
---
[Source](https://blog.talosintelligence.com/revault-when-your-soc-turns-against-you/)
