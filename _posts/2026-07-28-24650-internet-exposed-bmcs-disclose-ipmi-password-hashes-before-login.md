---
title: '24,650 Internet-Exposed BMCs Disclose IPMI Password Hashes Before Login'
date: 2026-07-28
permalink: /posts/2026/07/28/24650-internet-exposed-bmcs-disclose-ipmi-password-hashes-before-login/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique sur les interfaces BMC : risque massif d'exposition IPMI

Plus de 36 000 interfaces de gestion de serveurs (Baseboard Management Controller - BMC) sont exposées sur Internet, utilisant le protocole IPMI. Parmi elles, 24 650 divulguent des hashs de mots de passe avant même l'authentification, facilitant des attaques par force brute hors ligne.

**Points clés :**
*   **Vulnérabilité inhérente :** Le problème provient de la spécification IPMI v2.0 elle-même, rendant impossible un correctif logiciel classique.
*   **Attaque hors ligne :** Contrairement à une attaque par force brute classique, l'attaquant récupère le hash via une simple requête sur le port UDP 623 et peut tester des millions de combinaisons sans alerter le serveur.
*   **Risque accru :** L'usage massif de GPU permet désormais de casser les mots de passe par défaut (souvent prévisibles) en quelques minutes, facilitant la prise de contrôle totale de serveurs (persistance, contournement de l'OS, vol de données multi-locataires).

**Vulnérabilité identifiée :**
*   **CVE-2013-4786 :** Faille de divulgation d'informations (Score CVSS 7.5) permettant d'obtenir des hashs de mots de passe via des réponses RAKP.

**Recommandations de sécurité :**
*   **Isolation réseau :** Bloquer strictement l'accès au port UDP 623 au niveau de la passerelle réseau (périmètre).
*   **Segmentation :** Placer les interfaces BMC sur un réseau de gestion dédié, isolé et strictement contrôlé.
*   **Gestion des identifiants :** Remplacer immédiatement tous les mots de passe d'usine par des mots de passe robustes et uniques lors du déploiement.
*   **Durcissement :** Désactiver les versions obsolètes du protocole (IPMI 1.5) et restreindre l'accès aux interfaces via des politiques de contrôle d'accès réseau (ACL).

---
[Source](https://thehackernews.com/2026/07/24650-internet-exposed-bmcs-disclose.html){:target="_blank"}
