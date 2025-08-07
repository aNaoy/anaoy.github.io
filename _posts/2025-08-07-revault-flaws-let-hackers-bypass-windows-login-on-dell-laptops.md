---
title: 'ReVault flaws let hackers bypass Windows login on Dell laptops'
date: 2025-08-07
permalink: /posts/2025/08/07/revault-flaws-let-hackers-bypass-windows-login-on-dell-laptops/
tags:
- veille-cyber
- bleepingcomp
---
**Failles ReVault sur PC Dell : Contournement de la connexion Windows et persistance malveillante**

Des vulnérabilités dans le micrologiciel ControlVault3, affectant plus de 100 modèles d'ordinateurs portables Dell, permettent aux attaquants de contourner la connexion Windows et d'installer des logiciels malveillants capables de persister même après une réinstallation complète du système d'exploitation. Ces failles, surnommées "ReVault" par Cisco Talos, touchent le micrologiciel ControlVault3 et ses interfaces de programmation d'applications (API) Windows sur les gammes Latitude et Precision de Dell.

**Points Clés :**

*   Les failles permettent l'exécution de code arbitraire sur le micrologiciel, créant des implants persistants.
*   Un attaquant local avec accès physique peut exploiter ces vulnérabilités pour contourner la connexion Windows ou élever ses privilèges au niveau administrateur.
*   L'exploitation peut également permettre la manipulation de l'authentification par empreinte digitale, acceptant n'importe quelle empreinte.
*   Dell a publié des mises à jour de sécurité pour corriger ces failles.

**Vulnérabilités Identifiées (Famille ReVault) :**

*   Dépassement de tampon (Out-of-bounds flaws) : CVE-2025-24311, CVE-2025-25050
*   Vulnérabilité d'allocation mémoire arbitraire (Arbitrary free vulnerability) : CVE-2025-25215
*   Dépassement de pile (Stack overflow) : CVE-2025-24922
*   Désérialisation non sécurisée (Unsafe deserialization) : CVE-2025-24919

**Recommandations :**

*   Appliquer les mises à jour de sécurité fournies par Dell.
*   Désactiver les périphériques de sécurité inutilisés tels que les lecteurs d'empreintes digitales, lecteurs de cartes à puce et lecteurs NFC.
*   Désactiver la connexion par empreinte digitale dans les situations à haut risque.
*   Activer la détection d'intrusion du châssis dans les paramètres du BIOS pour signaler toute tentative de manipulation physique.
*   Activer la sécurité de connexion renforcée (Enhanced Sign-in Security - ESS) dans Windows pour détecter une configuration incorrecte du micrologiciel CV.

---
[Source](https://www.bleepingcomputer.com/news/security/revault-flaws-let-hackers-bypass-windows-login-on-dell-laptops/){:target="_blank"}
