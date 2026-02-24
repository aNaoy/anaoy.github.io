---
title: 'Microsoft adds Copilot data controls to all storage locations'
date: 2026-02-24
permalink: /posts/2026/02/24/microsoft-adds-copilot-data-controls-to-all-storage-locations/
tags:
- veille-cyber
- bleepingcomp
---
**Contrôle Étendu des Données pour Copilot dans Microsoft 365**

Microsoft étend ses politiques de prévention des pertes de données (DLP) pour mieux protéger les informations sensibles lorsqu'elles sont traitées par son assistant IA Copilot. Désormais, ces contrôles s'appliqueront aux documents Word, Excel et PowerPoint, quel que soit leur emplacement de stockage, y compris sur les appareils locaux. Auparavant, les politiques DLP ne couvraient que les fichiers stockés sur SharePoint ou OneDrive.

Cette mise à jour, qui sera déployée entre fin mars et fin avril 2026 via le composant Augmentation Loop (AugLoop) d'Office, permettra à Copilot de ne pas lire ni traiter les documents marqués comme restreints par les contrôles DLP. Les organisations ayant déjà configuré des politiques pour bloquer le traitement de contenus sensibles par Copilot n'auront aucune action à entreprendre, car la mise à jour sera activée automatiquement.

Le mécanisme sous-jacent repose sur une amélioration de la manière dont AugLoop accède aux étiquettes de sensibilité des fichiers. Au lieu de passer par Microsoft Graph via une URL de fichier, AugLoop pourra désormais lire directement l'étiquette de sensibilité depuis le client Office, uniformisant ainsi l'application des politiques DLP sur tous les emplacements de stockage.

Cette évolution intervient suite à un incident récent où un bogue dans Microsoft 365 Copilot Chat a permis à l'outil de lire et de résumer des emails confidentiels dans les dossiers "Éléments envoyés" et "Brouillons", malgré les politiques DLP actives. Bien que Microsoft ait précisé que seules les personnes autorisées avaient accès aux résumés, ce comportement n'était pas conforme à l'expérience utilisateur prévue, qui vise à exclure le contenu protégé de l'accès par Copilot.

**Points Clés :**

*   Extension des contrôles DLP de Microsoft 365 Copilot à tous les emplacements de stockage (locaux, SharePoint, OneDrive).
*   Amélioration du composant Augmentation Loop (AugLoop) d'Office pour une lecture directe des étiquettes de sensibilité des fichiers.
*   Automatisation de l'activation pour les organisations disposant de politiques DLP préexistantes.
*   Réponse aux demandes des clients pour une protection cohérente des données.

**Vulnérabilités :**

*   Aucune CVE spécifique n'est mentionnée dans l'article, mais un "code issue" a précédemment permis à Copilot de lire et résumer des emails confidentiels, malgré les protections DLP.

**Recommandations :**

*   Pour les administrateurs : Aucune action n'est requise si les politiques DLP existantes sont déjà configurées pour bloquer le traitement de contenus sensibles par Copilot.
*   Pour les utilisateurs : Comprendre que les contrôles DLP sont étendus pour mieux protéger les informations sensibles lors de l'utilisation de Copilot.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-adds-copilot-data-controls-to-all-storage-locations/){:target="_blank"}
