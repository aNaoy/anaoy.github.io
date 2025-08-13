---
title: 'Microsoft Patch Tuesday, August 2025 Edition'
date: 2025-08-13
permalink: /posts/2025/08/13/microsoft-patch-tuesday-august-2025-edition/
tags:
- veille-cyber
- krebs
---
**Mises à jour de sécurité Microsoft : Focus sur les vulnérabilités critiques d'août 2025**

Microsoft a publié des mises à jour corrigeant plus de 100 failles de sécurité dans ses systèmes d'exploitation Windows et autres logiciels. Treize de ces vulnérabilités sont classées comme "critiques", permettant potentiellement à des acteurs malveillants d'obtenir un accès à distance aux systèmes Windows sans interaction utilisateur significative.

**Points clés et vulnérabilités notables :**

*   **CVE-2025-53786** : Une vulnérabilité dans Microsoft Exchange Server qui permet à un attaquant de passer d'un serveur compromis à l'environnement cloud d'une organisation, potentiellement pour prendre le contrôle d'Exchange Online et d'autres services Microsoft Office 365 connectés. Cette faille affecte Exchange Server 2016, Exchange Server 2019 et Exchange Server Subscription Edition. Sa correction nécessite plus qu'une simple installation de patch, impliquant des instructions manuelles pour créer un service dédié afin de sécuriser la connexion hybride.

*   **CVE-2025-53779** : Une faiblesse dans le système d'authentification Windows Kerberos. Identifiée sous le nom de "BadSuccessor", cette faille, découverte par Akamai, permet à un attaquant non authentifié d'obtenir des privilèges d'administrateur de domaine. L'attaque exploite une faille dans le compte de service géré délégué (dMSA), une fonctionnalité introduite dans Windows Server 2025.

*   **CVE-2025-53766** : Une vulnérabilité d'exécution de code à distance dans le composant Windows GDI+, responsable du rendu graphique.

*   **CVE-2025-50165** : Une autre faiblesse dans le rendu graphique avec un score CVSS élevé.

*   **CVE-2025-53733** : Une vulnérabilité dans Microsoft Word qui peut être exploitée sans interaction utilisateur, potentiellement via le volet de visualisation.

*   **CVE-2025-53778** : Un défaut dans Windows NTLM, une fonction clé de l'authentification réseau de Windows. Cette faille pourrait permettre à un attaquant disposant d'un accès réseau limité et de privilèges utilisateur basiques d'élever ses privilèges au niveau SYSTEM. L'exploitation de cette faille est considérée comme "plus probable".

**Recommandations :**

*   **Mise à jour immédiate** : Les utilisateurs doivent installer les dernières mises à jour de sécurité de Microsoft pour corriger ces vulnérabilités.
*   **Actions spécifiques pour CVE-2025-53786** : En plus de l'installation du patch, il est crucial de suivre les instructions manuelles de Microsoft pour renforcer la sécurité des connexions hybrides Exchange.
*   **Fin de support pour Windows 10** : Microsoft cessera de fournir des mises à jour de sécurité gratuites pour Windows 10 après le 14 octobre 2025. Les utilisateurs de Windows 10 dont les machines ne répondent pas aux exigences matérielles de Windows 11 sont encouragés à envisager des alternatives comme Linux Mint pour continuer à utiliser leur matériel en toute sécurité.
*   **Test de Linux Mint** : Il est possible de tester Linux Mint à partir d'une clé USB sans installation préalable, offrant une transition potentiellement plus douce pour les utilisateurs habitués à Windows.

---
[Source](https://krebsonsecurity.com/2025/08/microsoft-patch-tuesday-august-2025-edition/){:target="_blank"}
