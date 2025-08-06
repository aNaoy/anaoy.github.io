---
title: 'ReVault! When your SoC turns against you…'
date: 2025-08-06
permalink: /posts/2025/08/06/revault-when-your-soc-turns-against-you/
tags:
- veille-cyber
- zerodaysfans
---
**ReVault : Menace sur la Sécurité Matérielle des PC Dell**

Des vulnérabilités critiques, baptisées "ReVault", ont été découvertes dans le firmware du Dell ControlVault3 (CV) et ses API Windows associées, affectant plus de 100 modèles d'ordinateurs portables Dell. Ces failles permettent des attaques de persistance post-compromission, capables de survivre aux réinstallations de Windows, et peuvent être exploitées pour contourner la connexion Windows ou obtenir des privilèges administrateur via un accès physique.

**Points Clés :**

*   **Produit Concerné :** Dell ControlVault3 et ControlVault3+ (une solution de sécurité matérielle stockant mots de passe et données biométriques).
*   **Modèles Affectés :** Plus de 100 modèles de portables Dell, notamment les séries Latitude et Precision.
*   **Impact Majeur :** Persistance post-compromission, contournement de la connexion, élévation de privilèges, compromission des données biométriques.

**Vulnérabilités Identifiées :**

*   **CVE-2025-24311** : Vulnérabilité hors limites affectant le firmware CV.
*   **CVE-2025-25050** : Vulnérabilité hors limites affectant le firmware CV.
*   **CVE-2025-25215** : Vulnérabilité d'allocation libre arbitraire affectant le firmware CV.
*   **CVE-2025-24922** : Vulnérabilité de dépassement de pile affectant le firmware CV.
*   **CVE-2025-24919** : Désérialisation non sécurisée affectant les API Windows du ControlVault.

**Scénarios d'Attaque :**

1.  **Pivot Post-Compromission :** Un utilisateur sans privilèges peut exécuter du code arbitraire sur le firmware CV via les API, permettant de voler des clés de chiffrement, de modifier le firmware et de créer un implant persistant.
2.  **Attaque Physique :** Un attaquant ayant un accès physique peut se connecter directement à la carte Unified Security Hub (USH) via USB pour exploiter les vulnérabilités. Il est ainsi possible de modifier le firmware pour accepter n'importe quelle empreinte digitale pour le déverrouillage, même sans connaître le mot de passe de l'utilisateur.

**Recommandations :**

*   **Mises à Jour Régulières :** Maintenir le système à jour pour installer le dernier firmware ControlVault.
*   **Désactivation :** Si les périphériques de sécurité (lecteur d'empreintes, lecteur de carte à puce, NFC) ne sont pas utilisés, envisager de désactiver les services ou le périphérique ControlVault.
*   **Sécurisation du Connexion :** Désactiver la connexion par empreinte digitale lorsque le risque est élevé. Activer la sécurité de connexion renforcée (ESS) de Windows peut aider à atténuer certaines attaques physiques.

**Détection :**

*   **Intrusion Physique :** Activer la détection d'intrusion dans le BIOS pour signaler toute manipulation physique.
*   **Journaux Windows :** Surveiller les plantages inattendus du service biométrique Windows ou des services de coffre-fort d'informations d'identification.
*   **Solutions de Sécurité :** Utiliser des signatures spécifiques (par exemple, pour Cisco Secure Endpoint : "bcmbipdll.dll Loaded by Abnormal Process").

---
[Source](https://blog.talosintelligence.com/revault-when-your-soc-turns-against-you/){:target="_blank"}
