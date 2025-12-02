---
title: 'Researchers Capture Lazarus APTs Remote-Worker Scheme Live on Camera'
date: 2025-12-02
permalink: /posts/2025/12/02/researchers-capture-lazarus-apts-remote-worker-scheme-live-on-camera/
tags:
- veille-cyber
- hackernews
---
**Lazarus et son réseau de faux employés informatiques**

Des chercheurs ont mis au jour un stratagème sophistiqué du groupe Lazarus, division Famous Chollima, exploitant des travailleurs informatiques à distance. Pour la première fois, les opérations de ces acteurs ont pu être observées en direct. Les chercheurs ont utilisé des environnements virtuels contrôlés par ANY.RUN pour simuler des postes de travail réels et ainsi capturer les activités des opérateurs.

Le modus operandi débute par une tentative de recrutement de faux développeurs américains. L'objectif est de servir de façade pour intégrer des employés nord-coréens dans des entreprises occidentales, particulièrement dans les secteurs de la finance, de la cryptomonnaie, de la santé et de l'ingénierie.

**Points clés de l'opération :**

*   **Recrutement:** Utilisation d'une fausse identité et de campagnes de recrutement via des plateformes comme LinkedIn.
*   **Entrevues simulées:** Emploi d'outils d'automatisation basés sur l'IA (Simplify Copilot, AiApply, Final Round AI) pour postuler et répondre aux questions d'entretien.
*   **Usurpation d'identité:** Collecte d'informations personnelles sensibles (SSN, ID, identifiants de messagerie) et utilisation de générateurs d'OTP en ligne pour contourner l'authentification à deux facteurs.
*   **Accès à distance:** Installation de Google Remote Desktop avec un code PIN fixe pour garantir un contrôle persistant.
*   **Infrastructure:** Utilisation du VPN Astrill, un schéma récurrent associé aux infrastructures de Lazarus.
*   **Objectif:** Prise de contrôle complète de l'identité et du poste de travail de la victime, sans nécessiter le déploiement de logiciels malveillants traditionnels.

**Vulnérabilités exploitées :**

L'article ne mentionne pas de CVE spécifiques, mais les vulnérabilités exploitées relèvent de :

*   **Ingénierie sociale et usurpation d'identité:** Les attaquants tirent parti de la confiance accordée lors des processus de recrutement et de la facilité d'usurpation d'identité.
*   **Failles dans les processus de recrutement à distance:** La difficulté de vérifier l'identité réelle des candidats et la dépendance aux outils en ligne peuvent être exploitées.
*   **Gestion laxiste des accès et des identifiants:** L'absence de vérifications rigoureuses lors de l'intégration de nouveaux employés ouvre la porte à des accès non autorisés.

**Recommandations :**

*   **Sensibilisation accrue:** Informer les équipes de recrutement et les employés sur les risques liés aux usurpations d'identité et aux tactiques de phishing ciblées.
*   **Vérification d'identité rigoureuse:** Mettre en place des processus de vérification d'identité robustes pour les nouveaux employés, notamment lors du recrutement à distance.
*   **Sécurisation des outils de recrutement et d'intégration:** S'assurer que les plateformes utilisées pour les entretiens et l'intégration sont sécurisées et que les accès sont correctement gérés.
*   **Surveillance des accès et des comportements suspects:** Surveiller les activités inhabituelles sur les postes de travail des employés, en particulier lors de la phase d'intégration.
*   **Environnements de test sécurisés:** Utiliser des environnements sandbox pour analyser les comportements potentiellement malveillants avant qu'ils n'impactent les systèmes de production.

---
[Source](https://thehackernews.com/2025/12/researchers-capture-lazarus-apts-remote.html){:target="_blank"}
