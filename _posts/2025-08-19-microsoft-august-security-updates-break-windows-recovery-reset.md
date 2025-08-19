---
title: 'Microsoft: August security updates break Windows recovery, reset'
date: 2025-08-19
permalink: /posts/2025/08/19/microsoft-august-security-updates-break-windows-recovery-reset/
tags:
- veille-cyber
- bleepingcomp
---
**Mises à jour d'août : Dysfonctionnement des fonctions de récupération et de réinitialisation sous Windows**

Les mises à jour de sécurité Windows d'août 2025 entraînent un dysfonctionnement des opérations de réinitialisation et de récupération sur les systèmes Windows 10 et les versions antérieures de Windows 11. Cette altération affecte la fonction "Réinitialiser mon PC" qui permet de conserver les fichiers, ainsi que l'outil "Résoudre les problèmes en utilisant Windows Update". Le dysfonctionnement concerne également les réinitialisations à distance via le fournisseur de services de configuration RemoteWipe (RemoteWipe CSP).

**Plateformes affectées :**

*   Windows 11 23H2 et Windows 11 22H2 (KB5063875)
*   Windows 10 22H2, Windows 10 Enterprise LTSC 2021, Windows 10 IoT Enterprise LTSC 2021 (KB5063709)
*   Windows 10 Enterprise LTSC 2019, Windows 10 IoT Enterprise LTSC 2019 (KB5063877)

**Recommandations :**

Microsoft est en cours de développement d'une solution qui sera déployée via des mises à jour hors bande pour toutes les plateformes concernées dans les prochains jours.

**Points clés :**

*   Les mises à jour de sécurité d'août 2025 provoquent des problèmes avec les fonctions de réinitialisation et de récupération de Windows.
*   Les réinitialisations partielles (conservation des fichiers) et complètes sont impactées.
*   Les réinitialisations à distance via RemoteWipe CSP sont également concernées.
*   Microsoft travaille sur un correctif qui sera déployé prochainement.

Il est à noter que Microsoft a récemment résolu d'autres problèmes liés aux mises à jour de sécurité, notamment des échecs de mise à jour à partir de partages réseau et des erreurs 0x80240069 lors de la distribution via WSUS. Des corrections ont également été apportées à des erreurs liées à l'enregistrement de certificats et à des problèmes de redémarrage de clusters et de machines virtuelles sur Windows Server.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-august-security-updates-break-windows-recovery-reset/){:target="_blank"}
