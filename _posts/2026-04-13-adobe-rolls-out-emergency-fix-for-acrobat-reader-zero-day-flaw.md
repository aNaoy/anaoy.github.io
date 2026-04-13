---
title: 'Adobe rolls out emergency fix for Acrobat, Reader zero-day flaw'
date: 2026-04-13
permalink: /posts/2026/04/13/adobe-rolls-out-emergency-fix-for-acrobat-reader-zero-day-flaw/
tags:
- veille-cyber
- bleepingcomp
---
### Correctif d'urgence pour une vulnérabilité zero-day dans Adobe Acrobat et Reader

Adobe a publié un correctif d'urgence pour remédier à une vulnérabilité zero-day activement exploitée depuis décembre 2025. Cette faille permet à un attaquant de contourner le bac à sable (sandbox) d'Adobe Acrobat et Reader via un fichier PDF malveillant, sans nécessiter d'interaction supplémentaire de la part de l'utilisateur.

**Points clés :**
* **Vecteur d'attaque :** L'ouverture d'un PDF piégé suffit à déclencher l'exécution de code arbitraire et l'exfiltration de données locales.
* **Méthode :** L'exploit détourne des API JavaScript privilégiées, notamment `util.readFileIntoStream()` pour la lecture de fichiers et `RSS.addFeed()` pour le transfert de données vers des serveurs tiers.
* **Impact :** La vulnérabilité a été observée dans des campagnes ciblées, utilisant notamment des documents en langue russe liés au secteur pétrolier et gazier.

**Vulnérabilité identifiée :**
* **CVE-2026-34621 :** Score de sévérité de 8.6. Affecte les versions d'Acrobat DC et Acrobat Reader DC (versions 26.001.21367 et antérieures) ainsi qu'Acrobat 2024 (versions 24.001.30356 et antérieures) sur Windows et macOS.

**Recommandations :**
* **Mise à jour immédiate :** Appliquer le correctif via l'outil de mise à jour intégré du logiciel (*Aide > Rechercher les mises à jour*) ou en téléchargeant la version corrigée sur le portail officiel d'Adobe.
* **Bonnes pratiques :** Faire preuve d'une extrême prudence avec les fichiers PDF provenant de sources non sollicitées et privilégier l'ouverture de documents suspects dans des environnements isolés ou sécurisés.

---
[Source](https://www.bleepingcomputer.com/news/security/adobe-rolls-out-emergency-fix-for-acrobat-reader-zero-day-flaw/){:target="_blank"}
