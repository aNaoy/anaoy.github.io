---
title: 'Microsoft removes PowerShell 2.0 from Windows 11, Windows Server'
date: 2025-08-13
permalink: /posts/2025/08/13/microsoft-removes-powershell-20-from-windows-11-windows-server/
tags:
- veille-cyber
- bleepingcomp
---
**Retrait de PowerShell 2.0 de Windows : Un changement pour la sécurité et la modernité**

Microsoft procède au retrait définitif de PowerShell 2.0 des futures versions de Windows 11 (à partir de la version 24H2) et de Windows Server 2025. Cette décision fait suite à une longue période de dépréciation initiée il y a huit ans. Le processus de retrait a débuté en juillet 2025 pour les utilisateurs du canal Canary de Windows 11.

Ce changement vise à réduire la complexité du système, à supprimer le code obsolète et à renforcer la sécurité globale de Windows.

**Points Clés :**

*   **Dépréciation Prolongée :** PowerShell 2.0, introduit avec Windows 7, était déprécié depuis 2017.
*   **Retrait Progressif :** Le retrait commence en août 2025 pour Windows 11 v24H2 et en septembre 2025 pour Windows Server 2025.
*   **Impact sur les Utilisateurs :** Les clients utilisant des scripts ou des applications héritées dépendant spécifiquement de PowerShell 2.0 devront prendre des mesures.
*   **Alternatives Supportées :** PowerShell 5.1 et PowerShell 7.x restent disponibles et supportés, offrant une compatibilité ascendante pour la majorité des commandes.

**Vulnérabilités :**

Bien que l'article ne mentionne pas de CVE spécifiques directement liées au retrait de PowerShell 2.0, le fait de supprimer une version ancienne et potentiellement moins sécurisée contribue à atténuer les risques de sécurité associés aux composants obsolètes. L'article suggère que l'utilisation de versions plus récentes est "plus sûre".

**Recommandations :**

*   **Mise à Jour des Scripts et Logiciels :** Les utilisateurs dont les applications ou scripts dépendent de PowerShell 2.0 doivent les mettre à jour pour assurer la compatibilité avec PowerShell 5.1 ou PowerShell 7.x.
*   **Remplacement des Outils Anciens :** Les logiciels obsolètes qui ne fonctionnent qu'avec PowerShell 2.0 doivent être remplacés.
*   **Tests :** Il est conseillé de tester les applications et scripts dans des environnements plus récents avant le retrait définitif pour éviter toute interruption de service.
*   **Contournements :** Pour les cas où la mise à jour n'est pas immédiatement possible, des solutions de contournement devront être envisagées.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-removes-powershell-20-from-windows-11-windows-server/){:target="_blank"}
