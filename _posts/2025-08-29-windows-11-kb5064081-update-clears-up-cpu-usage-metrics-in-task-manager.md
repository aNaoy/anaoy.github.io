---
title: 'Windows 11 KB5064081 update clears up CPU usage metrics in Task Manager'
date: 2025-08-29
permalink: /posts/2025/08/29/windows-11-kb5064081-update-clears-up-cpu-usage-metrics-in-task-manager/
tags:
- veille-cyber
- bleepingcomp
---
**Mise à jour Windows 11 : Un Gestionnaire des tâches plus précis et de nouvelles fonctionnalités**

La mise à jour cumulative optionnelle KB5064081 pour Windows 11 24H2 apporte des améliorations significatives, notamment une refonte de l'affichage de l'utilisation du processeur dans le Gestionnaire des tâches. Historiquement, la métrique "Utilitaire CPU" pouvait être trompeuse, ignorant le nombre de cœurs et comparant la fréquence de base plutôt que l'actuelle. Désormais, le Gestionnaire des tâches utilise une formule unifiée pour un calcul cohérent sur toutes ses sections, alignée sur les standards de l'industrie et les outils tiers. Une colonne "Utilitaire CPU" héritée reste disponible en option dans l'onglet "Détails" pour ceux qui préfèrent l'ancien affichage.

Cette mise à jour inclut également de nombreuses autres nouveautés déployées progressivement :

**Points Clés et Nouveautés :**

*   **Gestionnaire des tâches :** Affichage unifié et plus précis de l'utilisation du CPU.
*   **Recall :** Une page d'accueil personnalisée mettant en avant les activités récentes, les applications et sites les plus utilisés, avec des options de filtrage pour la confidentialité.
*   **Click to Do :** Un tutoriel interactif pour faciliter l'accomplissement de tâches via des actions sur texte et images.
*   **Permissions des applications :** Une nouvelle boîte de dialogue système repensée pour les demandes d'accès aux capacités du périphérique (localisation, caméra, microphone), avec un écran légèrement assombri et la boîte de dialogue centrée pour plus de visibilité.
*   **Centre de notifications :** Le retour de l'horloge avec secondes, affichée au-dessus de la date.
*   **Barre des tâches :**
    *   Une vue en grille améliorée pour la recherche d'images.
    *   Informations de statut plus claires pour la recherche, indiquant l'avancement de l'organisation des fichiers et la disponibilité des données (en ligne ou locale).
*   **Écran de verrouillage :** Davantage d'options de widgets et personnalisation (Météo, Liste de surveillance, Sports, Trafic, etc.).
*   **Explorateur de fichiers :**
    *   Séparateurs pour les icônes de premier niveau dans le menu contextuel.
    *   Affichage des icônes de personnes et des cartes de profil dans la section "Recommandé" pour les comptes professionnels ou scolaires, indiquant les connexions aux fichiers.
    *   Correction d'un bug lié au déblocage de fichiers dans les propriétés.
*   **Windows Hello :** Une interface repensée pour une communication plus claire et rapide, supportant les flux d'authentification comme les clés d'accès. L'amélioration de la reconnaissance faciale et la robustesse de la connexion par empreinte digitale après veille sont également mentionnées.
*   **Paramètres :**
    *   Des notifications d'activation et d'expiration Windows plus cohérentes avec le design de Windows 11.
    *   Une nouvelle section pour gérer les applications utilisant l'IA générative.
    *   Amélioration de l'agent dans les paramètres pour les PC Copilot+ (maintenant compatible avec les processeurs AMD et Intel, mais uniquement en anglais).
    *   Correction d'un problème de plantage lors de l'ajout d'une clé de sécurité.
*   **Tableau de widgets :** Plusieurs tableaux de bord disponibles et une expérience visuelle améliorée pour le flux "Découvrir".
*   **Sauvegarde Windows pour les organisations :** Généralement disponible pour des transitions de périphériques fluides.
*   **PowerShell 2.0 :** Sera retiré de Windows 11 24H2 en août 2025, les utilisateurs de scripts anciens devront être mis à jour.
*   **Correctifs divers :** Améliorations pour les légendes d'accessibilité, les claviers IME (chinois, japonais), la gestion des plantages d'applications (textinputframework.dll, dbgcore.dll), Kerberos, la connexion, Miracast et les services audio. Des correctifs spécifiques sont également cités pour la gestion des appareils, le système de fichiers ReFS, les claviers tactiles et les performances sur les appareils ARM64.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec des identifiants CVE n'est mentionnée dans cet article.

**Recommandations :**

*   Installer la mise à jour KB5064081 via "Paramètres" > "Windows Update" pour bénéficier des nouvelles fonctionnalités et des corrections.
*   Pour les utilisateurs de scripts ou d'outils dépendant de PowerShell 2.0, prévoir une mise à jour pour assurer la compatibilité avec les futures versions de Windows 11.

**Problèmes Connus :**

*   Erreurs incorrectes liées à CertificateServicesClient (CertEnroll).
*   Latence ou saccades dans les performances audio et vidéo lors de l'utilisation de NDI pour le streaming ou le transfert de flux. Un correctif est en cours de déploiement pour les erreurs CertEnroll.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/windows-11-kb5064081-update-clears-up-cpu-usage-metrics-in-task-manager/){:target="_blank"}
