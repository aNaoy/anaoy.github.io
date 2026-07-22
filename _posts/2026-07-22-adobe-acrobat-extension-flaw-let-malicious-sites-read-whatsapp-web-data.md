---
title: 'Adobe Acrobat Extension Flaw Let Malicious Sites Read WhatsApp Web Data'
date: 2026-07-22
permalink: /posts/2026/07/22/adobe-acrobat-extension-flaw-let-malicious-sites-read-whatsapp-web-data/
tags:
- veille-cyber
- hackernews
---
### HermeticReader : Vulnérabilité critique dans l'extension Adobe Acrobat

Une faille de sécurité majeure, baptisée **HermeticReader**, a été identifiée dans l'extension Adobe Acrobat pour Google Chrome. Elle permettait à un attaquant de contourner la politique de même origine (*Same-Origin Policy*) du navigateur pour exfiltrer silencieusement des données personnelles, notamment celles de WhatsApp Web.

**Points clés :**
*   **Impact massif :** Plus de 314 millions d'utilisateurs étaient potentiellement exposés.
*   **Mécanisme d'attaque :** En incitant la victime à visiter une page web piégée, l'attaquant pouvait injecter des commandes dans le moteur interne de l'extension pour manipuler le DOM (Document Object Model) de WhatsApp Web.
*   **Exfiltration :** L'attaquant pouvait récupérer la liste des contacts, les noms de profil, les aperçus de messages et le texte des conversations ouvertes sans avoir besoin d'installer de logiciel malveillant ou de voler des cookies de session.

**Vulnérabilité :**
*   **CVE-2026-48294** (Score CVSS : 7.4) : Vulnérabilité de type *Universal Cross-Site Scripting* (UXSS) permettant la divulgation de données entre différentes origines.
*   **Versions affectées :** Toutes les versions de l'extension (ID : `efaidnbmnnnibpcajpcglclefindmkaj`) antérieures à la version 26.5.2.2.

**Recommandations :**
*   **Mise à jour immédiate :** Vérifier que l'extension Adobe Acrobat Chrome est à jour (version 26.5.2.2 ou supérieure).
*   **Prudence sur le web :** Bien que la faille soit corrigée, l'exploitation reposait sur l'interaction de l'utilisateur avec des sites web malveillants ; il est donc conseillé de rester vigilant face aux liens provenant de sources non fiables.

---
[Source](https://thehackernews.com/2026/07/adobe-acrobat-extension-flaw-let.html){:target="_blank"}
