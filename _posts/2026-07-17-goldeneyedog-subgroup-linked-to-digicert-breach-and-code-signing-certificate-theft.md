---
title: 'GoldenEyeDog Subgroup Linked to DigiCert Breach and Code-Signing Certificate Theft'
date: 2026-07-17
permalink: /posts/2026/07/17/goldeneyedog-subgroup-linked-to-digicert-breach-and-code-signing-certificate-theft/
tags:
- veille-cyber
- hackernews
---
### Compromission de DigiCert par le groupe CylindricalCanine

Le groupe **CylindricalCanine**, un sous-groupe du collectif chinois **GoldenEyeDog** (aussi appelé APT-Q-27 ou Dragon Breath), a compromis l'autorité de certification DigiCert en avril 2026. Les attaquants ont infiltré les postes de travail d'analystes du support technique pour détourner des certificats de signature de code, utilisés ensuite pour signer leurs propres logiciels malveillants et échapper à la détection.

**Points clés :**
*   **Mode opératoire :** Utilisation d'ingénierie sociale via les canaux de support client (fichiers ZIP déguisés en captures d'écran).
*   **Charge utile :** Déploiement de **Golden Gh0st RAT** (une variante du cheval de Troie d'accès distant Gh0st RAT/Farfli) via une technique de *DLL side-loading*.
*   **Impact :** DigiCert a dû révoquer 60 certificats compromis, dont 27 ont été activement utilisés pour signer le malware « Zhong Stealer ».
*   **Vecteur d'accès :** Exploitation d'une fonction interne de support permettant d'accéder aux comptes clients. L'accès aux codes d'initialisation a suffi à usurper l'émission de certificats EV (Extended Validation).

**Vulnérabilités :**
*   **Défaillance logique :** Le modèle de menace interne ne prenait pas en compte la visibilité des codes d'initialisation sensibles par les comptes d'analystes via le portail de support. Aucune CVE spécifique n'est associée, car il s'agit d'une vulnérabilité de conception métier corrigée par une mise à jour logicielle (masquage des codes).

**Recommandations :**
*   **Protection des processus métier :** Masquer les codes d'initialisation sensibles et les données confidentielles aux interfaces de support technique, même pour les comptes internes (principe du moindre privilège).
*   **Sécurisation du support :** Renforcer la sensibilisation des équipes de support face aux fichiers suspects reçus via les chats clients.
*   **Surveillance accrue :** Mettre en œuvre des systèmes de détection pour identifier l'utilisation inhabituelle de certificats de signature de code et surveiller les comportements typiques des RAT (persistance, enregistrement de frappes, tunnel SOCKS).
*   **Validation des accès :** Restreindre les fonctionnalités de "vue client" dans les portails de gestion de certificats pour limiter les risques en cas de compromission d'un compte employé.

---
[Source](https://thehackernews.com/2026/07/goldeneyedog-subgroup-linked-to.html){:target="_blank"}
