---
title: 'KONNI Adopts AI to Generate PowerShell Backdoors'
date: 2026-01-22
permalink: /posts/2026/01/22/konni-adopts-ai-to-generate-powershell-backdoors/
tags:
- veille-cyber
- zerodaysfans
---
**Le groupe KONNI exploite l'IA pour le développement de portes dérobées PowerShell**

Une campagne de phishing attribuée au groupe d'acteurs malveillants nord-coréen KONNI cible des développeurs et des équipes d'ingénierie, notamment dans la région APAC (Japon, Australie, Inde). L'objectif semble être d'infiltrer des environnements de développement liés aux technologies blockchain afin d'accéder à des ressources sensibles.

Ce qui distingue cette campagne est l'utilisation d'une porte dérobée PowerShell générée par une intelligence artificielle. Cette approche innovante pour un groupe connu témoigne de l'adoption croissante d'outils basés sur l'IA par les cybercriminels. La campagne utilise une chaîne d'infection en plusieurs étapes, commençant par un lien menant à un fichier ZIP contenant un document leurre et un raccourci Windows (LNK). L'exécution du LNK déclenche un chargeur PowerShell qui décompresse d'autres fichiers malveillants, dont la porte dérobée.

**Points Clés :**

*   **Expansion géographique :** KONNI élargit ses cibles au-delà de la Corée du Sud, touchant le Japon, l'Australie et l'Inde.
*   **Ciblage spécialisé :** La campagne vise spécifiquement les professionnels du développement logiciel et de l'ingénierie travaillant sur des projets blockchain.
*   **Utilisation de l'IA :** Une porte dérobée PowerShell générée par IA est déployée, caractérisée par une structure de code propre, une documentation détaillée et des commentaires typiques d'une génération par LLM (Large Language Model).
*   **Techniques d'évasion :** La porte dérobée intègre des mécanismes d'anti-analyse, d'évasion de sandbox, et un UAC bypass (User Account Control bypass) via la technique fodhelper pour obtenir des privilèges élevés.
*   **Persistance :** La persistance est assurée par la création de tâches planifiées, parfois déguisées en tâches légitimes (ex: OneDrive Startup Task).
*   **Communication C2 :** La communication avec le serveur de commande et de contrôle (C2) utilise un mécanisme de défi JavaScript AES pour contourner les protections anti-bot.

**Vulnérabilités exploitées (implicites) :**

*   Les vulnérabilités sociales (phishing, ingénierie sociale) sont utilisées pour inciter les victimes à exécuter le fichier malveillant.
*   Des techniques de contournement de l'UAC sont utilisées pour élever les privilèges sur le système compromis.

**Recommandations :**

*   **Sensibilisation à la sécurité :** Former les employés à identifier et signaler les courriels et les liens suspects.
*   **Contrôles d'accès stricts :** Mettre en œuvre le principe du moindre privilège et une gestion rigoureuse des droits d'administration.
*   **Surveillance des journaux et des activités réseau :** Examiner les journaux système pour détecter des comportements anormaux et surveiller le trafic réseau sortant suspect.
*   **Mises à jour et correctifs :** Maintenir les systèmes d'exploitation et les logiciels à jour pour corriger les vulnérabilités connues.
*   **Solutions de sécurité de point de terminaison :** Utiliser des solutions antivirus et de détection et réponse avancées (EDR) capables de détecter les malwares et les comportements suspects.
*   **Blocage des domaines et adresses IP malveillantes :** Configurer les pare-feu et les systèmes de sécurité pour bloquer les communications avec les domaines et adresses IP répertoriés comme malveillants.

**Indications de compromission (IOCs) :** Des hachages de fichiers, des noms de domaines et des adresses IP associés à cette campagne sont disponibles dans l'article complet.

---
[Source](https://research.checkpoint.com/2026/konni-targets-developers-with-ai-malware/){:target="_blank"}
