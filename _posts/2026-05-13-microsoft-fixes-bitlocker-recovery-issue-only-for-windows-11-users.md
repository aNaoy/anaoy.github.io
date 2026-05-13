---
title: 'Microsoft fixes BitLocker recovery issue only for Windows 11 users'
date: 2026-05-13
permalink: /posts/2026/05/13/microsoft-fixes-bitlocker-recovery-issue-only-for-windows-11-users/
tags:
- veille-cyber
- bleepingcomp
---
### Correctif BitLocker : Résolution partielle pour Windows 11

Une mise à jour Microsoft (avril 2026) provoque le blocage de certains systèmes en mode de récupération BitLocker après l'installation des correctifs de sécurité. Ce problème survient principalement sur des configurations d'entreprise utilisant des paramètres de stratégie de groupe (GPO) spécifiques liés au TPM.

**Points clés :**
*   **Problème :** Le système demande une clé de récupération BitLocker lors du redémarrage suite à une mise à jour, en raison de conflits avec la validation du TPM (notamment les configurations PCR7 non valides).
*   **Disponibilité du correctif :** Le correctif KB5089549 est actuellement disponible uniquement pour **Windows 11 25H2**.
*   **Plateformes impactées :** Windows 10, Windows 11 et Windows Server. Les utilisateurs particuliers sont peu touchés, le problème affectant surtout les parcs gérés par des administrateurs système.
*   **Vulnérabilité :** Aucune CVE spécifique n'est associée à cet incident, il s'agit d'un dysfonctionnement opérationnel lié à une configuration de stratégie de groupe "non recommandée".

**Recommandations pour les administrateurs :**
*   **Action immédiate :** Supprimer la stratégie de groupe « Configurer le profil de validation de plateforme TPM pour les configurations de microprogramme UEFI natives » avant de déployer les mises à jour d'avril 2026.
*   **Configuration :** S'assurer que les liaisons BitLocker utilisent le profil PCR7 standard.
*   **Attente :** Pour les environnements Windows 10 et Windows Server, patienter jusqu'à la publication d'un correctif permanent par Microsoft.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-bitlocker-recovery-issue-only-for-windows-11-users/){:target="_blank"}
