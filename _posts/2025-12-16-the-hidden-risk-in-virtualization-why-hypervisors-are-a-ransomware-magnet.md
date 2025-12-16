---
title: 'The Hidden Risk in Virtualization: Why Hypervisors are a Ransomware Magnet'
date: 2025-12-16
permalink: /posts/2025/12/16/the-hidden-risk-in-virtualization-why-hypervisors-are-a-ransomware-magnet/
tags:
- veille-cyber
- bleepingcomp
---
### Les hyperviseurs, nouvelle cible privilégiée des rançongiciels

Les infrastructures virtualisées, au cœur de nombreuses opérations informatiques modernes, font l'objet d'une attention croissante de la part des cybercriminels. Les acteurs de menace ciblent désormais les hyperviseurs, les logiciels qui gèrent les machines virtuelles, pour démultiplier l'impact de leurs attaques, notamment par le biais de rançongiciels. Cette tendance s'explique par la difficulté d'appliquer des protections de sécurité traditionnelles, telles que les solutions EDR, directement sur la couche de l'hyperviseur, créant ainsi un angle mort pour les défenseurs.

Le groupe de rançongiciels Akira est identifié comme un acteur majeur dans cette évolution, exploitant les vulnérabilités de cette couche critique. La compromission d'un hyperviseur peut potentiellement mettre en péril des dizaines, voire des centaines, de machines virtuelles simultanément. L'utilisation d'outils intégrés comme openssl pour le chiffrement permet aux attaquants de contourner la nécessité de déployer des binaires de rançongiciel personnalisés.

**Points Clés :**

*   **Augmentation des attaques de rançongiciels sur les hyperviseurs :** Une augmentation significative a été observée, passant de 3% à 25% des cas en l'espace de six mois.
*   **Ciblage des couches basses :** Les attaquants cherchent à contourner les défenses des systèmes d'exploitation et des réseaux en s'attaquant à la fondation de la virtualisation.
*   **Impact démultiplié :** La compromission d'un hyperviseur permet un contrôle étendu sur de multiples systèmes invités.
*   **Évitement des protections classiques :** Les rançongiciels peuvent être déployés directement via l'hyperviseur, sans passer par les machines virtuelles.

**Vulnérabilités et Exploitations observées :**

*   **Utilisation de crédits d'authentification internes compromis :** Permet de gagner un contrôle élevé sur plusieurs systèmes.
*   **Abus des utilitaires de gestion de l'hyperviseur :** Modification des paramètres des machines virtuelles, désactivation des défenses, préparation au déploiement de rançongiciels.
*   **CVE-2024-37085 :** Permet de contourner l'authentification et d'obtenir un contrôle administratif complet sur un hôte ESXi avec des permissions AD suffisantes, entraînant un chiffrement massif des VM en quelques secondes. L'exploit tire parti de l'octroi automatique de privilèges administratifs au groupe 'ESX Admins' d'Active Directory.
*   **Exposition de protocoles non sécurisés :** Les interfaces de gestion non corrigées ou les protocoles exposés comme le Service Location Protocol (SLP) servent de points d'entrée faciles.

**Recommandations de Sécurité :**

*   **Sécurisation de l'accès et moindre privilège :**
    *   Utiliser des comptes locaux dédiés pour la gestion de l'hyperviseur, éviter les comptes administrateur de domaine.
    *   Mettre en œuvre l'authentification multifacteur (MFA) obligatoire pour toutes les interfaces de gestion critiques.
    *   Utiliser des mots de passe robustes, stockés dans un gestionnaire de mots de passe sécurisé.
    *   Segmenter le réseau de gestion de l'hyperviseur des réseaux de production et utilisateurs.
    *   Déployer une "jump box" ou un serveur bastion pour centraliser et auditer l'accès administratif.
    *   Appliquer le principe du moindre privilège (PoLP) pour les accès au plan de contrôle (vCenter, hôtes).
    *   Restreindre l'accès aux interfaces de gestion à des périphériques d'administration dédiés.

*   **Verrouillage de l'environnement d'exécution de l'hyperviseur :**
    *   Activer le paramètre avancé `VMkernel.Boot.execInstalledOnly = TRUE` pour n'autoriser l'exécution que de binaires signés.
    *   Désactiver ou fermer les services inutiles (SSH, ESXi Shell) et activer le mode "lockdown".

*   **Maintien des correctifs et minimisation des surfaces d'exposition :**
    *   Maintenir un inventaire précis des hôtes ESXi et de leurs niveaux de patch.
    *   Prioriser les correctifs de sécurité du fournisseur pour les vulnérabilités liées à l'hyperviseur.
    *   Désactiver ou restreindre les services non nécessaires, comme SLP (port 427).
    *   Ne pas exposer directement les hôtes ESXi à Internet pour la gestion ; utiliser des VPN, des bastions ou des réseaux de gestion isolés.

*   **Stratégie de sauvegarde et capacité de récupération rapide :**
    *   Adopter la règle de sauvegarde "3-2-1" (trois copies, deux supports différents, une hors site).
    *   Utiliser des dépôts de sauvegarde immuables ou des snapshots.
    *   Ne pas connecter le dépôt de sauvegarde à Active Directory ; utiliser des comptes locaux dédiés.
    *   S'assurer que les sauvegardes incluent des images complètes de VM et l'état de l'hyperviseur.
    *   Tester régulièrement les sauvegardes et effectuer des exercices de récupération complets.

*   **Surveillance, détection d'anomalies et défense en profondeur :**
    *   Transférer les journaux ESXi vers un SIEM et créer des alertes pour les événements suspects (connexion root, activation de service, changement de niveau d'acceptation VIB, démontage de datastore).
    *   Surveiller les dérives de configuration (mode lockdown désactivé, SSH activé, `execInstalledOnly` désactivé).
    *   Journaliser le trafic réseau de gestion pour détecter les accès inhabituels, les tentatives de mouvement latéral ou les schémas d'E/S de datastore suspects.
    *   Adopter une approche de confiance zéro pour la gestion de l'hyperviseur.
    *   Surveiller spécifiquement les fichiers de journaux critiques : `/var/log/auth.log`, `/var/log/hostd.log`, `/var/log/shell.log`, et `/var/log/vobd.log`.
    *   Envisager un modèle de responsabilité partagée avec des prestataires SOC/MDR externes, en complétant leur surveillance par une expertise interne pour le contexte métier.

---
[Source](https://www.bleepingcomputer.com/news/security/the-hidden-risk-in-virtualization-why-hypervisors-are-a-ransomware-magnet/){:target="_blank"}
