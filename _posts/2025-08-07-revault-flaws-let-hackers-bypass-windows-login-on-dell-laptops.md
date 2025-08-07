---
title: 'ReVault flaws let hackers bypass Windows login on Dell laptops'
date: 2025-08-07
permalink: /posts/2025/08/07/revault-flaws-let-hackers-bypass-windows-login-on-dell-laptops/
tags:
- veille-cyber
- bleepingcomp
---
**Failles ReVault : Risque de contournement de la sécurité sur les portables Dell**

Des vulnérabilités dans le micrologiciel ControlVault3, affectant plus de 100 modèles de portables Dell, ouvrent la porte aux attaquants pour contourner l'authentification Windows et installer des logiciels malveillants persistants, même après une réinstallation du système. Ces failles, découvertes par Cisco Talos et nommées "ReVault", touchent le micrologiciel ControlVault3 et ses interfaces de programmation d'applications (API) sous Windows, particulièrement sur les gammes Latitude et Precision prisées dans les environnements sensibles.

**Points Clés et Vulnérabilités :**

*   **Bypass de connexion Windows et escalade de privilèges :** L'exploitation combinée de ces failles permet une exécution de code arbitraire sur le micrologiciel, rendant possibles des implants permanents. Un attaquant local avec un accès physique peut contourner la connexion Windows ou obtenir des privilèges d'administrateur.
*   **Manipulation de l'authentification biométrique :** Il est possible de compromettre l'authentification par empreinte digitale pour qu'elle accepte n'importe quelle empreinte.
*   **Accès physique facilité :** L'accès à la carte fille de sécurité (Unified Security Hub - USH) via USB avec un connecteur personnalisé permet à un attaquant d'exploiter les vulnérabilités sans devoir se connecter au système ni connaître le mot de passe du chiffrement complet du disque.
*   **Vulnerabilités spécifiques (CVE) :**
    *   `CVE-2025-24311`, `CVE-2025-25050` : Failles hors limites (Out-of-bounds flaws).
    *   `CVE-2025-25215` : Vulnérabilité d'allocation de mémoire arbitraire (Arbitrary free).
    *   `CVE-2025-24922` : Dépassement de tampon de pile (Stack overflow).
    *   `CVE-2025-24919` : Problème de désérialisation non sécurisée (Unsafe deserialization) affectant les API Windows de ControlVault.

**Recommandations :**

*   **Mise à jour du système :** Appliquer les mises à jour de sécurité Dell pour le pilote et le micrologiciel ControlVault3 via Windows Update ou le site de Dell.
*   **Désactivation des périphériques inutilisés :** Désactiver les lecteurs d'empreintes digitales, lecteurs de cartes à puce et lecteurs NFC lorsqu'ils ne sont pas utilisés.
*   **Désactivation de l'authentification par empreinte digitale :** Envisager sa désactivation dans les situations à haut risque.
*   **Activation de la détection d'intrusion du châssis :** Configurer le BIOS pour signaler toute tentative d'altération physique.
*   **Activation de Enhanced Sign-in Security (ESS) :** Utiliser cette fonctionnalité dans Windows pour détecter les anomalies dans le micrologiciel de ControlVault.

---
[Source](https://www.bleepingcomputer.com/news/security/revault-flaws-let-hackers-bypass-windows-login-on-dell-laptops/){:target="_blank"}
