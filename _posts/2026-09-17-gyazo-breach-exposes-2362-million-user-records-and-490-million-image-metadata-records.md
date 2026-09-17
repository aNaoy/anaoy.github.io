---
title: 'Gyazo Breach Exposes 23.62 Million User Records and 490 Million Image Metadata Records'
date: 2026-09-17
permalink: /posts/2026/09/17/gyazo-breach-exposes-2362-million-user-records-and-490-million-image-metadata-records/
tags:
- veille-cyber
- hackernews
---
### Violation massive de données chez Gyazo : 23 millions d'utilisateurs exposés

Le service de partage d'images Gyazo a subi une intrusion majeure ayant entraîné l'exposition de 23,62 millions de comptes utilisateurs et 490 millions de métadonnées d'images. L'attaquant a exploité une vulnérabilité sur le serveur d'upload d'images pour exécuter des commandes arbitraires et accéder à la base de données.

**Points clés :**
*   **Données compromises :** Noms, emails, mots de passe hashés, IDs utilisateurs, tokens d'intégration (X/Google), statistiques d'utilisation et historique de facturation (sans données bancaires).
*   **Exposition des images :** Les IDs des images ont été dérobés, compromettant potentiellement la confidentialité des captures privées, car ces IDs servent de clés d'accès directes. Des métadonnées sensibles, incluant des données de géolocalisation EXIF et du texte extrait par OCR, ont également été exfiltrées.
*   **Chronologie :** L'activité suspecte a été détectée le 11 septembre. La vulnérabilité a été corrigée le 12 septembre, mais la brèche n'a été officiellement notifiée que le 16 septembre.

**Vulnérabilités :**
*   Aucun identifiant CVE n'a été publié à ce jour. La faille concerne une **vulnérabilité non spécifiée dans le serveur d'upload d'images** permettant l'exécution de commandes à distance (RCE).

**Recommandations :**
*   **Changement immédiat des mots de passe :** Les utilisateurs sont invités à modifier leur mot de passe Gyazo ainsi que celui de tout autre service utilisant les mêmes identifiants.
*   **Vigilance accrue :** Surveiller les e-mails et messages suspects (phishing) liés à cet incident.
*   **Gestion des comptes tiers :** Révoquer l'accès aux comptes intégrés (X, Google) si des activités anormales sont détectées.

---
[Source](https://thehackernews.com/2026/09/gyazo-breach-exposes-2362-million-user.html){:target="_blank"}
