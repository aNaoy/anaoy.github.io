---
title: 'Hackers Compromised 14,500+ Dahua Devices Using Credential Attacks, Auth Bypasses, and P2P'
date: 2026-08-19
permalink: /posts/2026/08/19/hackers-compromised-14500-dahua-devices-using-credential-attacks-auth-bypasses-and-p2p/
tags:
- veille-cyber
- hackernews
---
### Opération CameraSwarm : compromission massive de dispositifs Dahua

L'opération « CameraSwarm » a permis de compromettre plus de 14 530 appareils Dahua entre juin et juillet 2026. Cette campagne, utilisant des outils de piratage retrouvés dans un répertoire exposé, a principalement touché des équipements en Ukraine et en Russie. Les attaquants ont combiné des attaques par force brute (identifiants), l'exploitation de vulnérabilités connues et le détournement de protocoles P2P.

**Points clés :**
*   **Méthodes d'attaque :** 13 229 appareils compromis par attaques sur les identifiants, 1 923 via des failles de contournement d'authentification et 283 via le relais P2P.
*   **Persistance :** Certains accès malveillants ont été configurés pour persister, même après une réinitialisation d'usine sur certains firmwares.
*   **Vecteur P2P :** L'exploitation du protocole P2P (Easy4IP) permet de contourner les protections NAT, rendant les caméras accessibles directement via leur numéro de série.

**Vulnérabilités exploitées :**
*   **CVE-2021-33044 :** Contournement de l'authentification (CVSS 9.8).
*   **CVE-2021-33045 :** Contournement de l'authentification (CVSS 9.8).
*   **Exposition P2P :** Problématique de conception (non CVE) permettant l'établissement d'un relais vers l'appareil avant toute vérification d'authentification sur les versions de firmware antérieures à mi-2024.

**Recommandations :**
*   **Mise à jour :** Installer immédiatement les dernières versions de firmware fournies par Dahua.
*   **Configuration P2P :** Désactiver la fonction P2P (Easy4IP) si elle n'est pas strictement nécessaire.
*   **Gestion des accès :** Utiliser des mots de passe robustes et uniques, supprimer les comptes inutilisés et auditer régulièrement la liste des comptes actifs.
*   **Segmentation réseau :** Isoler le système de vidéosurveillance sur un sous-réseau dédié pour limiter la portée d'une éventuelle intrusion.

---
[Source](https://thehackernews.com/2026/08/hackers-compromised-14500-dahua-devices.html){:target="_blank"}
