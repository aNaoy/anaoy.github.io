---
title: 'An analysis of incidents at Brazilian educational institutions'
date: 2026-08-03
permalink: /posts/2026/08/03/an-analysis-of-incidents-at-brazilian-educational-institutions/
tags:
- veille-cyber
- securelist
---
### Analyse des cybermenaces dans les institutions éducatives brésiliennes

Les institutions éducatives brésiliennes font face à une recrudescence d'attaques cybernétiques ciblant des données sensibles. La complexité de ces environnements, où cohabitent étudiants, chercheurs et personnel administratif, rend la gestion des accès particulièrement difficile.

**Points clés :**
*   **Profil des cibles :** 60 % des institutions attaquées sont privées. Les établissements privés sont davantage visés par les rançongiciels, tandis que les institutions publiques font face à des tentatives d'escalade de privilèges.
*   **Vecteurs d'accès initiaux :** Utilisation de comptes valides (identifiants compromis), exploitation d'applications exposées et menaces internes.
*   **Outils et techniques :** Usage fréquent d'outils légitimes détournés (AnyDesk, PsExec), d'outils de capture d'écran/clavier et de familles de rançongiciels comme *LockBit 3* et *DragonForce*.
*   **Vulnérabilités :** Maintien de systèmes obsolètes (Windows 10 après fin de support, Windows Server 2016 sans patch), absence d'authentification multifacteur (MFA) et partage de comptes utilisateurs.

**Vulnérabilités et techniques identifiées (MITRE ATT&CK) :**
*   **Privilèges :** Exploitation via des variantes "Potato" (GodPotato, SweetPotato, BadPotato).
*   **Techniques notables :**
    *   T1586 (Compromise Accounts)
    *   T1056.001 (Keylogging)
    *   T1068 (Exploitation for Privilege Escalation)
    *   T1219 (Remote Access Tools)
    *   T1486 (Data Encrypted for Impact)

**Recommandations :**
1.  **Authentification :** Implémenter le MFA sur tous les services accessibles à distance (VPN, portails, emails).
2.  **Gestion des accès :** Appliquer le principe du moindre privilège, interdire les comptes partagés et révoquer les permissions administratives inutiles.
3.  **Mise à jour :** Établir une politique stricte de gestion des correctifs pour éliminer les systèmes obsolètes.
4.  **Outils de contrôle :** Restreindre et surveiller étroitement l'installation d'outils d'accès distant (AnyDesk, TeamViewer).
5.  **Résilience :** Isoler les sauvegardes de l'environnement principal et les tester régulièrement.
6.  **Forensique :** Améliorer la visibilité via une journalisation centralisée et la rétention de données EDR pour faciliter la reconstruction des incidents.

---
[Source](https://securelist.com/incidents-at-brazilian-educational-institutions/120803/){:target="_blank"}
