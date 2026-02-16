---
title: 'Building a Secure Electron Auto-Updater'
date: 2026-02-16
permalink: /posts/2026/02/16/building-a-secure-electron-auto-updater/
tags:
- veille-cyber
- zerodaysfans
---
### Renforcer la Sécurité des Mises à Jour Automatiques dans les Applications Electron

Les mécanismes de mise à jour automatique des applications Electron présentent des risques de sécurité significatifs, car ils s'exécutent souvent avec des privilèges élevés et peuvent devenir un vecteur d'exécution de code à distance s'ils sont compromis. Les solutions actuelles comme `autoUpdater` d'Electron et `electron-updater` d'Electron-Builder, bien qu'utiles, ne protègent pas entièrement contre certaines classes d'attaques, notamment en raison des limitations des systèmes d'exploitation en matière de validation de l'intégrité logicielle.

**Points Clés :**

*   **Vecteur d'Attaque :** Les mises à jour automatiques sont une cible attrayante pour les attaquants. Un compromis équivaut à une exécution de code à distance.
*   **Limites des Solutions Existantes :** Les mécanismes intégrés peuvent être vulnérables à des attaques spécifiques faute de garanties d'intégrité robustes au niveau du système d'exploitation.
*   **SafeUpdater :** Un projet de référence conçu pour améliorer la sécurité des mises à jour dans Electron, en se basant sur des principes de conception axés sur les menaces.

**Vulnérabilités et Menaces Non Adressées par les Solutions Courantes :**

*   **Attaque par Rétrogradation (Downgrade Attack) :**
    *   **Vecteur :** Manipulation du manifeste de mise à jour ou des métadonnées pour proposer d'anciennes versions.
    *   **Impact :** Réintroduction de vulnérabilités connues.
*   **Attaque d'Intégrité :**
    *   **Vecteur :** Modification non autorisée des binaires de mise à jour, des installateurs ou des métadonnées via un canal de distribution compromis ou une attaque Man-in-the-Middle (MITM).
    *   **Impact :** Exécution de code arbitraire.
*   **Attaque par Condition de Course (Race Condition) :**
    *   **Vecteur :** Remplacement de fichiers de mise à jour vérifiés entre la vérification et l'installation, nécessitant un accès local.
    *   **Impact :** Exécution de code malveillant, escalade de privilèges.
*   **Attaque par Version Non Testée :**
    *   **Vecteur :** Proposition de versions non destinées à la production (alpha/bêta) via le canal de mise à jour, notamment si les clés de signature ou les canaux sont partagés entre environnements.
    *   **Impact :** Exposition à des fonctionnalités non révisées, à de nouvelles vulnérabilités.

**Recommandations et Solutions Proposées par SafeUpdater :**

SafeUpdater intègre plusieurs mécanismes pour contrer ces menaces :

*   **Vérification de Signature Ed25519 :**
    *   Tous les composants de mise à jour sont signés cryptographiquement avec Ed25519. Une clé publique intégrée dans l'application permet de vérifier l'authenticité et l'intégrité.
    *   Liaison cryptographique de la mise à jour à une version spécifique pour prévenir les attaques par rétrogradation (`SHA-256(fichier) + version`).
*   **Vérifications d'Intégrité SHA-512 :**
    *   En plus de la signature, les binaires de mise à jour sont vérifiés via leur hachage SHA-512, stocké dans le manifeste signé. Cela assure l'intégrité de bout en bout.
*   **Manifestes de Version Immuables :**
    *   Les métadonnées de mise à jour sont distribuées via des manifestes immuables et signés, empêchant leur falsification pour pointer vers des emplacements malveillants ou réintroduire des versions vulnérables.
*   **Gestion Sécurisée des Fichiers Temporaires :**
    *   Les fichiers temporaires sont stockés dans des répertoires restreints avec des permissions limitées au propriétaire pour atténuer les attaques par condition de course. La vérification et l'installation s'effectuent sur le même chemin de fichier.

**Configuration de SafeUpdater :**

*   `updatesPublicKey` : Clé publique Ed25519 hexadécimale pour la vérification des signatures.
*   `updatesUrl` : URL de base du serveur de mise à jour.
*   `updatesEnabled` : Interrupteur principal pour activer/désactiver le système de mise à jour.
*   `certificateAuthority` (Optionnel) : Certificat PEM pour la validation TLS.
*   `allowInsecureTLS` (Optionnel, `false` par défaut) : Désactive la validation des certificats TLS (à n'utiliser qu'en développement).
*   `downgradeEnabled` (Optionnel, `false` par défaut) : Permet les rétrogradations cryptographiquement vérifiées.

Le projet fournit également des outils pour générer des clés, signer les artefacts et déployer un serveur de développement HTTPS pour tester le processus de mise à jour. SafeUpdater est conçu comme une base solide pour des mécanismes de mise à jour plus robustes, bien qu'il nécessite des tests approfondis avant une utilisation en production.

---
[Source](https://blog.doyensec.com/2026/02/16/electron-safe-updater.html){:target="_blank"}
