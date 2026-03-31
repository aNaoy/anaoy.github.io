---
title: 'Microsoft fixes Outlook Classic crashes caused by Teams Meeting add-in'
date: 2026-03-31
permalink: /posts/2026/03/31/microsoft-fixes-outlook-classic-crashes-caused-by-teams-meeting-add-in/
tags:
- veille-cyber
- bleepingcomp
---
### Résolution du bug de plantage dans Outlook Classic lié à Microsoft Teams

Microsoft a déployé un correctif pour résoudre une instabilité majeure affectant le client Outlook classique. Depuis la mi-mars 2026, l'utilisation simultanée de versions obsolètes d'Outlook et de la nouvelle version du module complémentaire « Teams Meeting Add-in » (v1.26.02603) provoquait des plantages répétitifs de l'application, forçant le démarrage en mode sans échec. Aucun identifiant CVE n'a été associé à cet incident de stabilité.

**Points clés :**
*   **Cause :** Incompatibilité entre les anciennes versions d'Outlook (build <= 2402) et la mise à jour récente du module complémentaire Teams.
*   **Statut :** Problème résolu par la mise à jour vers Microsoft Teams version 26058.712.4527.9297.
*   **Contexte :** Cet incident s'ajoute à une série de dysfonctionnements récents sur Outlook Classic, incluant des erreurs de synchronisation Gmail/Yahoo, des difficultés d'ouverture d'e-mails chiffrés et des problèmes d'affichage du curseur de la souris.

**Recommandations :**
*   **Mise à jour prioritaire :** Mettre à jour le client Outlook classique vers la version la plus récente.
*   **Solution alternative (Réparation) :** Si la mise à jour directe n'est pas possible, effectuer une « Réparation en ligne » via les paramètres d'installation d'Office.
*   **Contournement manuel :** En cas d'impossibilité de mise à jour, désactiver le module incriminé :
    1. Lancer Outlook en mode sans échec (maintenir `Ctrl` au démarrage).
    2. Accéder à **Fichier > Options > Compléments > Gérer : Compléments COM > Atteindre**.
    3. Décocher **Microsoft Teams Meeting Add-in for Microsoft Office** et valider.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-outlook-classic-crashes-caused-by-teams-meeting-add-in/){:target="_blank"}
