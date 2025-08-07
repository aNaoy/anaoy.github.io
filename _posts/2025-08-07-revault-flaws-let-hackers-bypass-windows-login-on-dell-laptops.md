---
title: 'ReVault flaws let hackers bypass Windows login on Dell laptops'
date: 2025-08-07
permalink: /posts/2025/08/07/revault-flaws-let-hackers-bypass-windows-login-on-dell-laptops/
tags:
- veille-cyber
- bleepingcomp
---
**Vulnérabilités "ReVault" sur les ordinateurs portables Dell : Accès et persistance**

Cinq vulnérabilités, regroupées sous le nom de code "ReVault", ont été découvertes dans le firmware ControlVault3 et ses interfaces de programmation d'applications (API) sous Windows, affectant de nombreux modèles d'ordinateurs portables professionnels Dell (Latitude, Precision). Ces failles permettent à des attaquants d'outrepasser le processus de connexion Windows, d'exécuter du code arbitraire sur le firmware, et d'installer des logiciels malveillants capables de persister même après une réinstallation du système d'exploitation. L'accès physique à l'appareil est un prérequis pour exploiter ces vulnérabilités. L'exploitation peut également mener à la manipulation des authentifications biométriques, permettant à n'importe quelle empreinte digitale d'être acceptée.

**Points Clés :**

*   **Contournement de la connexion Windows :** Possibilité de se connecter à un système sans connaître les identifiants légitimes.
*   **Persistance des malwares :** Des implants peuvent survivre aux réinstallations de Windows.
*   **Escalade de privilèges :** Permet d'obtenir des droits d'administrateur localement.
*   **Manipulation biométrique :** Possibilité de falsifier l'authentification par empreinte digitale pour accepter toute empreinte.
*   **Accès physique requis :** L'exploitation nécessite un accès physique pour interagir directement avec la carte de sécurité (USH).

**Vulnérabilités identifiées :**

*   Flaws out-of-bounds (CVE-2025-24311, CVE-2025-25050)
*   Vulnérabilité d'arbitrary free (CVE-2025-25215)
*   Stack overflow (CVE-2025-24922)
*   Problème de désérialisation non sécurisée (CVE-2025-24919)

**Recommandations :**

*   **Mise à jour des systèmes :** Appliquer les correctifs de sécurité publiés par Dell via Windows Update ou le site du fabricant.
*   **Désactivation des périphériques de sécurité inutilisés :** Désactiver les lecteurs d'empreintes digitales, lecteurs de cartes à puce et lecteurs NFC lorsque non utilisés.
*   **Désactivation de l'authentification par empreinte digitale :** Recommandé dans les situations à haut risque.
*   **Activation de la détection d'intrusion du châssis :** Configurer cette option dans le BIOS pour signaler toute tentative de manipulation physique.
*   **Activation de la sécurité de connexion renforcée (ESS) dans Windows :** Pour détecter une utilisation inappropriée du firmware ControlVault.

---
[Source](https://www.bleepingcomputer.com/news/security/revault-flaws-let-hackers-bypass-windows-login-on-dell-laptops/){:target="_blank"}
