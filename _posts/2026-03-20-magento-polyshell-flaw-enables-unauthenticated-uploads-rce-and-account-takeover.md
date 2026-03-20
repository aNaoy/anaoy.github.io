---
title: 'Magento PolyShell Flaw Enables Unauthenticated Uploads, RCE and Account Takeover'
date: 2026-03-20
permalink: /posts/2026/03/20/magento-polyshell-flaw-enables-unauthenticated-uploads-rce-and-account-takeover/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique "PolyShell" dans Magento

Une faille de sécurité majeure, baptisée **PolyShell**, affecte l'API REST de Magento Open Source et Adobe Commerce (versions jusqu'à 2.4.9-alpha2). Cette vulnérabilité permet à des attaquants non authentifiés de télécharger des fichiers malveillants déguisés en images, menant à une exécution de code à distance (RCE) ou à une prise de contrôle de compte (via XSS stocké).

**Points clés :**
*   **Vecteur d'attaque :** L'API REST de Magento traite mal les options de produits de type "fichier", enregistrant des données encodées en base64 directement dans le répertoire `pub/media/custom_options/quote/`.
*   **Contexte :** Bien qu'Adobe ait corrigé le problème dans une version préliminaire (référence de sécurité **APSB25-94**), aucune mise à jour corrective isolée n'est disponible pour les versions en production actuelles.
*   **Contexte global :** Cette vulnérabilité émerge alors qu'une campagne de défiguration massive touche actuellement des milliers de sites Magento, bien que le lien direct avec PolyShell reste à confirmer.

**Vulnérabilités :**
*   **Type :** Téléchargement de fichiers non restreint (Unrestricted File Upload).
*   **CVE :** Non explicitement mentionnée par identifiant unique dans l'article, mais référencée sous le bulletin de sécurité Adobe **APSB25-94**.

**Recommandations :**
*   **Restreindre l'accès :** Configurer le serveur web (Nginx ou Apache) pour interdire l'exécution de scripts dans le répertoire `pub/media/custom_options/`.
*   **Audit de sécurité :** Scanner régulièrement le serveur à la recherche de web shells, portes dérobées ou fichiers suspects.
*   **Protection périmétrique :** Utiliser un pare-feu applicatif web (WAF) spécialisé pour filtrer les tentatives de téléchargement malveillantes, car la simple restriction de répertoire ne bloque pas l'upload lui-même.

---
[Source](https://thehackernews.com/2026/03/magento-polyshell-flaw-enables.html){:target="_blank"}
