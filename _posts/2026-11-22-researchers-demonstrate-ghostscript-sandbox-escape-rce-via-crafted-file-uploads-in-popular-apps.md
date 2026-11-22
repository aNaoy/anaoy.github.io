---
title: 'Researchers Demonstrate Ghostscript Sandbox-Escape RCE via Crafted File Uploads in Popular Apps'
date: 2026-11-22
permalink: /posts/2026/11/22/researchers-demonstrate-ghostscript-sandbox-escape-rce-via-crafted-file-uploads-in-popular-apps/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans Ghostscript : contournement de sandbox et exécution de code

Une faille de sécurité majeure dans **Ghostscript** (l'interpréteur utilisé par de nombreuses applications Linux pour traiter des fichiers comme les PDF ou les images) permet à un attaquant de s'échapper du bac à sable (sandbox) pour exécuter des commandes arbitraires sur le serveur hôte.

**Points clés :**
*   **Vecteur d'attaque :** La vulnérabilité est déclenchée par des fichiers malveillants soumis à des applications traitant automatiquement des documents (aperçus, vignettes, impression, formulaires d'upload).
*   **Propagation indirecte :** Il n'est pas nécessaire que l'application appelle Ghostscript directement ; des bibliothèques courantes (ImageMagick, Pillow, libvips, plugins Qt) peuvent transmettre involontairement le fichier malveillant au moteur vulnérable.
*   **Impact :** L'exécution de code se produit avec les privilèges du service effectuant le rendu. Des démonstrations ont prouvé que des services publics (files d'attente d'impression, formulaires web WordPress, courriels) peuvent être exploités sans authentification préalable.

**Vulnérabilités identifiées :**
*   **CVE-2026-125396 :** Faille de type *use-after-free* dans le module de chargement des polices de Ghostscript, permettant de désactiver le mécanisme de sécurité `-dSAFER`. Corrigée dans la version **10.08.0**.
*   **CVE-2026-65640 :** Vulnérabilité spécifique traitée dans WordPress (version 7.0.4) pour bloquer le vecteur d'entrée initial.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer le correctif Ghostscript (v10.08.0+) et mettre à jour les applications dépendantes (ex: WordPress 7.0.4+). 
*   **Attention aux conteneurs :** S'assurer que les versions de Ghostscript intégrées dans les images Docker ou les environnements conteneurisés sont également mises à jour, car une mise à jour de l'OS hôte ne suffit pas.
*   **Mesures de durcissement (Hardening) :**
    *   Restreindre les types de fichiers autorisés lors des téléchargements.
    *   Exiger une authentification pour les services sensibles (notamment les files d'attente d'impression).
    *   Implémenter des profils de sécurité système (type AppArmor) pour restreindre les capacités d'exécution de Ghostscript.

---
[Source](https://thehackernews.com/2026/11/researchers-demonstrate-ghostscript.html){:target="_blank"}
