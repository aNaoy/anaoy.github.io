---
title: 'Microsoft rolls out hardware-accelerated BitLocker in Windows 11'
date: 2025-12-24
permalink: /posts/2025/12/24/microsoft-rolls-out-hardware-accelerated-bitlocker-in-windows-11/
tags:
- veille-cyber
- bleepingcomp
---
**BitLocker Amélioré : Performances et Sécurité Accrues sous Windows 11**

La dernière mise à jour de Windows 11 intègre une fonction BitLocker optimisée par l'accélération matérielle. Cette évolution exploite les capacités des puces système (SoC) et des processeurs pour améliorer significativement les performances du chiffrement de disque complet, tout en renforçant la sécurité des données.

Auparavant, les opérations cryptographiques de BitLocker pouvaient impacter les performances, notamment lors de tâches intensives comme le jeu ou le montage vidéo, en raison de la charge sur le CPU. L'accélération matérielle décharge ces opérations vers des modules de sécurité matériels (HSM) intégrés aux SoC, libérant ainsi le processeur principal et offrant une expérience utilisateur plus fluide. Les tests montrent une réduction substantielle de l'utilisation du CPU par opération d'entrée/sortie.

Au-delà des gains de performance, cette nouvelle approche renforce la sécurité en protégeant mieux les clés de chiffrement. En les isolant davantage du CPU et de la mémoire, elle diminue leur exposition aux cyberattaques, complétant ainsi la protection déjà assurée par le module de plateforme sécurisée (TPM). L'objectif est de minimiser la présence des clés BitLocker dans le CPU et la mémoire.

Cette amélioration est disponible sur Windows 11 versions 24H2 (avec les mises à jour de septembre) et 25H2. Le support initial concerne les systèmes Intel vPro équipés des processeurs Intel Core Ultra Series 3 ("Panther Lake"), avec une extension progressive à d'autres fournisseurs de SoC.

**Points Clés :**

*   **Accélération Matérielle :** Exploitation des SoC pour décharger les opérations cryptographiques de BitLocker.
*   **Amélioration des Performances :** Réduction de l'impact sur le CPU, amélioration des activités gourmandes en ressources.
*   **Sécurité Renforcée :** Meilleure protection des clés de chiffrement, diminution de l'exposition aux attaques.
*   **Algorithme XTS-AES-256 :** Utilisation par défaut sur les appareils compatibles.
*   **Disponibilité :** Windows 11 24H2 et 25H2.

**Vulnérabilités :**

Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans cet article lié à l'implémentation de cette nouvelle fonctionnalité.

**Recommandations :**

*   Assurez-vous que votre système exécute Windows 11 24H2 (avec mises à jour de septembre) ou 25H2.
*   Vérifiez la compatibilité matérielle de votre appareil, notamment la présence d'un SoC prenant en charge l'accélération cryptographique.
*   Pour confirmer l'activation du mode accéléré matériel, exécutez la commande `manage-bde -status` et recherchez la mention "Hardware accelerated" sous "Encryption Method".
*   Notez que BitLocker reviendra par défaut au mode logiciel si des algorithmes ou des tailles de clé non pris en charge sont utilisés, ou si des politiques d'entreprise l'exigent, ou encore si le mode FIPS est activé sans la certification adéquate du SoC.

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-rolls-out-hardware-accelerated-bitlocker-in-windows-11/){:target="_blank"}
