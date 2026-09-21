---
title: 'Group Policy hijacked: PAYLOAD ransomware weaponizes Active Directory GPO'
date: 2026-09-21
permalink: /posts/2026/09/21/group-policy-hijacked-payload-ransomware-weaponizes-active-directory-gpo/
tags:
- veille-cyber
- securelist
---
### Menace sans chiffrement : L'abus des GPO par PAYLOAD

L'incident analysé illustre une tendance émergente de l'extorsion sans chiffrement (« encryptionless extortion »), où les attaquants exploitent l'infrastructure de confiance Active Directory (AD) pour paralyser les opérations au lieu de chiffrer les données. En détournant les objets de stratégie de groupe (GPO), les attaquants contournent les solutions de sécurité basées sur les fichiers ou les processus.

**Points clés :**
*   **Technique d'attaque :** Utilisation de GPO malveillants créés et liés à la racine du domaine, agissant comme un canal de distribution privilégié (SYSTEM).
*   **Impact :** Défacements visuels (fond d'écran, bannière de connexion), désactivation du compte administrateur local et coupe du pare-feu Windows sur l'ensemble du parc informatique.
*   **Persistance :** La persistance est ancrée dans la configuration AD elle-même, rendant inutile tout nettoyage local sur les postes de travail sans suppression préalable des GPO corrompus.
*   **Latence :** Une période de latence d'une journée a été observée entre la création des GPO et leur application effective lors du redémarrage des machines, masquant le lien temporel entre l'intrusion et l'impact.

**Vulnérabilités exploitées (MITRE ATT&CK) :**
*   **T1484.001 :** Modification de stratégie de groupe (abus de GPO).
*   **T1562.004 :** Désactivation du pare-feu via GPO.
*   **T1078 :** Utilisation de comptes valides (accès initial via VPN SSL).
*   **T1531 :** Suppression de l'accès aux comptes (désactivation de l'administrateur local).

**Recommandations :**

*   **Réponse immédiate :** Supprimer les GPO malveillants (`{C897F2C7-C2AC-4E6F-BF48-58036FF29E79}` et `{22099AD2-E062-4F56-B574-5099BBA4E7A6}`), nettoyer les fichiers dans le dossier `SYSVOL` et forcer un rafraîchissement des politiques (`gpupdate /force`).
*   **Audits AD :** Activer l'audit des changements du service d'annuaire (ID 5136, 5137, 5141) et monitorer l'intégrité des fichiers dans `SYSVOL`.
*   **Durcissement :**
    *   Séparer les droits de création de GPO des droits de liaison.
    *   Implémenter le modèle d'administration par niveaux (Tiered Administration).
    *   Déployer Windows LAPS pour la gestion des mots de passe administrateur locaux.
    *   Forcer l'authentification multi-facteurs (MFA) résistante au phishing pour tous les accès distants.
*   **Détection :** Créer des alertes SIEM sur les modifications de `gPLink` à la racine du domaine et sur toute création de fichiers suspects dans `SYSVOL` hors des processus de réplication légitimes.

---
[Source](https://securelist.com/tr/payload-ransomware-via-group-policy/121335/){:target="_blank"}
