---
title: 'TCLBANKER Banking Trojan Targets Financial Platforms via WhatsApp and Outlook Worms'
date: 2026-05-08
permalink: /posts/2026/05/08/tclbanker-banking-trojan-targets-financial-platforms-via-whatsapp-and-outlook-worms/
tags:
- veille-cyber
- hackernews
---
### TCLBANKER : Une nouvelle menace sophistiquée ciblant les institutions financières

**Points clés**
*   **Nature de la menace :** Le cheval de Troie bancaire « TCLBANKER » (suivi sous le nom de code REF3076) cible 59 plateformes financières, bancaires et de cryptomonnaies.
*   **Propagation :** Le malware intègre un module « ver » qui se diffuse via WhatsApp Web (en détournant les sessions) et Microsoft Outlook (en utilisant le compte de messagerie de la victime pour envoyer des emails de phishing), augmentant ainsi sa crédibilité.
*   **Techniques d'évasion :** Utilise le chargement latéral de DLL (*DLL side-loading*) sur une application légitime (Logitech Logi AI Prompt Builder), neutralise les outils d'analyse (ETW, débogueurs, sandboxes) et n'exécute sa charge utile qu'après vérification de l'environnement (notamment la langue système : portugais brésilien).
*   **Capacités :** Une fois actif, il peut enregistrer les frappes clavier, capturer des captures d'écran, manipuler le presse-papier, prendre le contrôle à distance et afficher de fausses interfaces de connexion pour le vol d'identifiants.

**Vulnérabilités exploitées**
*   **DLL Side-loading :** Exploitation du logiciel signé *Logi AI Prompt Builder* pour exécuter une DLL malveillante.
*   **Détournement d'applications légitimes :** Utilisation de WPPConnect pour automatiser WhatsApp et abus des API locales de Microsoft Outlook.
*   *Note : Aucune CVE spécifique n'est mentionnée, l'attaque repose sur des techniques de manipulation de processus (Living-off-the-land) plutôt que sur une faille logicielle unique.*

**Recommandations**
*   **Surveillance des terminaux :** Détecter les exécutions inhabituelles impliquant des processus signés, en particulier si ces derniers chargent des DLL non signées ou non attendues.
*   **Sécurisation des communications :** Sensibiliser les utilisateurs aux risques de propagation via WhatsApp Web et Outlook ; encourager la déconnexion systématique des sessions web.
*   **Contrôle des privilèges :** Restreindre les capacités des applications bureautiques à automatiser d'autres logiciels (via UI Automation ou interopérabilité COM).
*   **Détection comportementale :** Surveiller les appels système suspects et les tentatives de désactivation de l'ETW (Event Tracing for Windows) sur les postes de travail.

---
[Source](https://thehackernews.com/2026/05/tclbanker-banking-trojan-targets.html){:target="_blank"}
