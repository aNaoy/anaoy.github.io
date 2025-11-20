---
title: 'WhatsApp compromise leads to Astaroth deployment'
date: 2025-11-20
permalink: /posts/2025/11/20/whatsapp-compromise-leads-to-astaroth-deployment/
tags:
- veille-cyber
- sophos
---
### Campagne de maliciels via WhatsApp au Brésil

Une campagne de maliciels mult-étapes, baptisée STAC3150, cible les utilisateurs de WhatsApp au Brésil. Elle diffuse des archives contenant un script de téléchargement qui récupère ensuite plusieurs charges utiles.

**Points clés :**

*   La campagne utilise des messages sur WhatsApp, y compris la fonction "Visualisation unique", comme vecteur d'infection.
*   Les messages contiennent des archives ZIP avec des fichiers VBS ou HTA malveillants.
*   Ces fichiers exécutent PowerShell pour télécharger des charges utiles de second niveau.
*   Ces charges utiles incluent des scripts pour collecter des informations de contact WhatsApp et des données de session.
*   Une autre charge utile est un installateur MSI qui déploie le cheval de Troie bancaire Astaroth (également connu sous le nom de Guildma).
*   Les attaquants utilisent des scripts PowerShell ou Python, des outils comme Selenium et WPPConnect pour intercepter les sessions WhatsApp Web, voler des informations et distribuer du spam.
*   Le malware Astaroth s'installe via un script AutoIt et utilise des clés de registre pour assurer la persistance.
*   La majorité des victimes (95%) sont localisées au Brésil, mais des cas ont aussi été observés dans d'autres pays d'Amérique latine, aux États-Unis et en Autriche.

**Vulnérabilités exploitées :**

L'article ne mentionne pas de CVE spécifiques. Les vulnérabilités exploitées sont liées à :
*   L'ingénierie sociale incitant les utilisateurs à ouvrir des pièces jointes malveillantes.
*   La capacité d'exécuter des scripts PowerShell/Python et des fichiers VBS/HTA.
*   La compromission de sessions WhatsApp Web.
*   Les mécanismes d'auto-démarrage (clés de registre) pour la persistance.

**Recommandations :**

*   **Sensibilisation des employés :** Les organisations doivent informer leurs employés sur les risques liés à l'ouverture de pièces jointes, même si elles proviennent de contacts connus, envoyées via des plateformes de messagerie et de réseaux sociaux.
*   **Détection et prévention :** L'article liste plusieurs signatures de détection de Sophos (VBS/DwnLdr-ADJT, VBS/DwnLdr-ADJW, VBS/DwnLdr-ADJS, Troj/Mdrop-KEP, Troj/Mdrop-KES, Troj/AutoIt-DJB, Troj/HTADrp-CE).
*   **Surveillance des indicateurs de compromission :** Utiliser les noms de domaine associés aux serveurs de commande et de contrôle (C2) pour détecter l'activité suspecte :
    *   manoelimoveiscaioba[.]com
    *   varegjopeaks[.]com
    *   docsmoonstudioclayworks[.]online
    *   shopeeship[.]com
    *   miportuarios[.]com
    *   borizerefeicoes[.]com
    *   clhttradinglimited[.]com
    *   lefthandsuperstructures[.]com

---
[Source](https://news.sophos.com/en-us/2025/11/20/whatsapp-compromise-leads-to-astaroth-deployment/){:target="_blank"}
