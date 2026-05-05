---
title: 'Amazon SES increasingly abused in phishing to evade detection'
date: 2026-05-05
permalink: /posts/2026/05/05/amazon-ses-increasingly-abused-in-phishing-to-evade-detection/
tags:
- veille-cyber
- bleepingcomp
---
### Abus croissant d'Amazon SES pour contourner les filtres de phishing

Les attaquants exploitent de plus en plus le service Amazon SES (Simple Email Service) pour diffuser des campagnes de phishing sophistiquées. En utilisant cette infrastructure légitime et réputée, les emails malveillants passent les contrôles d'authentification standards (SPF, DKIM, DMARC), rendant les solutions de filtrage basées sur la réputation inefficaces.

**Points clés :**
* **Cause principale :** La fuite massive de clés d'accès AWS (IAM) dans des dépôts publics comme GitHub, des fichiers `.ENV` ou des buckets S3.
* **Automatisation :** Les attaquants utilisent des outils comme *TruffleHog* pour scanner et identifier automatiquement les secrets exposés, validant ensuite leurs privilèges pour envoyer des volumes massifs d'emails.
* **Techniques utilisées :** Création de templates HTML imitant des services de confiance, usurpation d'identité (type DocuSign) et fraudes complexes (BEC - Business Email Compromise) impliquant de fausses factures et des fils de discussion fabriqués.
* **Impact :** Le blocage des adresses IP d'Amazon est impossible sans perturber les communications légitimes, ce qui complique la défense.

**Vulnérabilités :**
Il ne s'agit pas d'une vulnérabilité logicielle (CVE) au sens strict, mais d'une **exposition de secrets/identifiants (Credential Exposure)**. Le manque de rotation des clés et l'absence de restriction d'accès aux ressources IAM permettent l'utilisation abusive du service.

**Recommandations :**
* **Principe du moindre privilège :** Restreindre strictement les permissions IAM accordées aux clés d'accès.
* **Sécurisation des accès :** Activer l'authentification multifacteur (MFA) et mettre en œuvre des restrictions d'accès basées sur les adresses IP.
* **Gestion des secrets :** Effectuer une rotation régulière des clés d'accès et empêcher le stockage de secrets dans des dépôts de code publics ou des fichiers non sécurisés.
* **Surveillance :** Signaler toute activité suspecte au service *AWS Trust & Safety*.

---
[Source](https://www.bleepingcomputer.com/news/security/amazon-ses-increasingly-abused-in-phishing-to-evade-detection/){:target="_blank"}
