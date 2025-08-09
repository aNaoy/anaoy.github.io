---
title: 'CyberArk and HashiCorp Flaws Enable Remote Vault Takeover Without Credentials'
date: 2025-08-09
permalink: /posts/2025/08/09/cyberark-and-hashicorp-flaws-enable-remote-vault-takeover-without-credentials/
tags:
- veille-cyber
- hackernews
---
**Escalade de Privilèges dans les Solutions de Gestion des Identités Fortes**

Des chercheurs en cybersécurité ont identifié une quinzaine de vulnérabilités critiques dans les solutions CyberArk Secrets Manager, Self-Hosted et Conjur Open Source, ainsi que dans HashiCorp Vault. Ces failles permettent à des attaquants distants d'accéder aux identifiants d'entreprise et d'en extraire des secrets et des jetons, potentiellement sans aucune authentification préalable.

**Points Clés :**

*   Ces vulnérabilités, regroupées sous le nom de "Vault Fault", affectent des fonctions essentielles telles que l'authentification, l'application des politiques et l'exécution des plugins.
*   Certaines failles, présentes depuis plusieurs années, permettent un contournement des mécanismes de sécurité, une élévation de privilèges, voire l'exécution de code à distance.
*   Les chercheurs ont démontré des chaînes d'exploitation permettant d'obtenir un accès non authentifié et de contrôler entièrement les coffres-forts.
*   Une fonctionnalité de sécurité peut être détournée pour servir de vecteur de ransomware.

**Vulnérabilités Identifiées (avec CVEs) :**

*   **CyberArk Secrets Manager :**
    *   CVE-2025-49827 (CVSS 9.1) : Contournement de l'authentificateur IAM.
    *   CVE-2025-49831 (CVSS 9.1) : Contournement de l'authentificateur IAM via un appareil réseau mal configuré.
    *   CVE-2025-49828 (CVSS 8.6) : Exécution de code à distance.
*   **HashiCorp Vault :**
    *   CVE-2025-6000 (CVSS 9.1) : Exécution de code arbitraire à distance via l'abus du catalogue de plugins.
    *   CVE-2025-5999 (CVSS 7.2) : Élévation de privilèges vers le niveau root via la normalisation des politiques.
    *   CVE-2025-6037 : Usurpation d'identité de certificat.
*   **Dell ControlVault3 Firmware (ReVault) :**
    *   CVE-2025-25050 (CVSS 8.8) : Écriture hors limites.
    *   CVE-2025-25215 (CVSS 8.8) : Libération arbitraire de mémoire.
    *   CVE-2025-24922 (CVSS 8.8) : Dépassement de tampon sur la pile entraînant l'exécution de code arbitraire.
    *   CVE-2025-24311 (CVSS 8.4) : Lecture hors limites entraînant une fuite d'informations.
    *   CVE-2025-24919 (CVSS 8.1) : Désérialisation d'entrées non fiables entraînant l'exécution de code arbitraire.

**Recommandations :**

*   Les utilisateurs de CyberArk Secrets Manager, Self-Hosted et Conjur Open Source doivent mettre à jour vers les versions :
    *   CyberArk Secrets Manager et Self-Hosted : 13.5.1 et 13.6.1
    *   CyberArk Conjur Open Source : 1.22.1
*   Les utilisateurs de HashiCorp Vault doivent mettre à jour vers les versions :
    *   Vault Community Edition : 1.20.2
    *   Vault Enterprise : 1.20.2, 1.19.8, 1.18.13, et 1.16.24
*   Pour les vulnérabilités ReVault affectant les appareils Dell :
    *   Appliquer les correctifs fournis par Dell.
    *   Désactiver les services ControlVault si les périphériques associés (lecteurs d'empreintes digitales, cartes à puce, NFC) ne sont pas utilisés.
    *   Désactiver la connexion par empreintes digitales dans les environnements à haut risque.
    *   Pour les attaques physiques, il est conseillé de ne pas connecter de périphériques inconnus et de faire attention aux manipulations physiques de l'appareil.

---
[Source](https://thehackernews.com/2025/08/cyberark-and-hashicorp-flaws-enable.html){:target="_blank"}
