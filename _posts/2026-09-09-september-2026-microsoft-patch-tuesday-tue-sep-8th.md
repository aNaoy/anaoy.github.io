---
title: 'September 2026 Microsoft Patch Tuesday, (Tue, Sep 8th)'
date: 2026-09-09
permalink: /posts/2026/09/09/september-2026-microsoft-patch-tuesday-tue-sep-8th/
tags:
- veille-cyber
- sans-isc
---
### Record de vulnérabilités : Patch Tuesday de septembre 2026

Le bulletin de sécurité Microsoft de septembre 2026 atteint un niveau historique avec **973 vulnérabilités corrigées**, dont 113 sont classées critiques. Deux failles font actuellement l'objet d'une exploitation active.

#### Points clés et vulnérabilités majeures

*   **CVE-2026-81963 (Windows Update Stack) :** Vulnérabilité d'élévation de privilèges (EOP) classée "Important" (CVSS 7.8). Exploitée dans la nature, elle permet à un attaquant local authentifié d'obtenir des privilèges SYSTEM sur Windows 11 et Server 2025.
*   **CVE-2026-85880 (Windows ALPC) :** Faille EOP par dépassement de tampon sur le tas (CVSS 7.8). Également exploitée dans la nature, elle permet à un attaquant en "AppContainer" de sortir du bac à sable et d'obtenir les privilèges SYSTEM sur diverses versions de Windows 10 et Server.
*   **CVE-2026-66302 (Skype for Business) :** Exécution de code à distance (RCE) critique (CVSS 9.8). Permet à un attaquant non authentifié d'écrire des fichiers arbitraires sur le serveur.
*   **CVE-2026-69579 (MSMQ - Windows Message Queuing) :** RCE critique (CVSS 9.8) basée sur une vulnérabilité de type "use-after-free". Exploitable à distance par l'envoi d'un paquet malveillant.
*   **CVE-2026-69590 (Windows RRAS) :** RCE critique (CVSS 9.8). Un attaquant non authentifié peut exécuter du code à distance en envoyant un paquet réseau spécifique au service RRAS.

#### Recommandations

1.  **Priorité immédiate :** Déployer sans délai les correctifs pour les deux failles déjà exploitées (**CVE-2026-81963** et **CVE-2026-85880**), particulièrement sur les postes exposés et les serveurs multi-utilisateurs.
2.  **Gestion des services critiques :**
    *   Appliquer les correctifs pour **Skype for Business**, **MSMQ** et **RRAS** en priorité absolue pour contrer les menaces RCE.
    *   Pour **MSMQ** : Si le service n'est pas indispensable, désactivez-le ou restreignez l'accès réseau (notamment le port TCP 1801).
    *   Pour **RRAS** : Désactivez le service si inutile, restreignez l'accès via pare-feu ou VPN, et surveillez les flux réseau anormaux vers ces hôtes.
3.  **Audit :** Pour les serveurs Skype, auditez les journaux et les contrôles d'accès à la recherche d'activités suspectes (écriture de fichiers ou exécution de code non autorisée).

---
[Source](https://isc.sans.edu/diary/rss/33320){:target="_blank"}
