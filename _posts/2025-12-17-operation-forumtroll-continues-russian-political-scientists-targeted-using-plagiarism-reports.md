---
title: 'Operation ForumTroll continues: Russian political scientists targeted using plagiarism reports'
date: 2025-12-17
permalink: /posts/2025/12/17/operation-forumtroll-continues-russian-political-scientists-targeted-using-plagiarism-reports/
tags:
- veille-cyber
- securelist
---
**Campagne ForumTroll : Viseurs Académiques par Fausses Rapports de Plagiat**

Une campagne de cyberattaque persistante, nommée Opération ForumTroll, a ciblé des universitaires russes spécialisés en sciences politiques, relations internationales et économie mondiale. Après une précédente vague d'attaques exploitant une vulnérabilité dans Google Chrome, la nouvelle phase, détectée en octobre 2025, utilise des courriels de phishing se faisant passer pour une bibliothèque scientifique électronique.

Ces courriels invitent les destinataires à télécharger un rapport de plagiat personnalisé, qui, une fois ouvert, déclenche le téléchargement d'une archive contenant un fichier raccourci malveillant. L'exécution de ce dernier lance un script PowerShell téléchargeant un chargeur qui utilise la technique du COM Hijacking pour assurer sa persistance et déploie le framework de "red teaming" commercial Tuoni. Une fausse page PDF de rapport de plagiat est également téléchargée et ouverte pour masquer l'activité.

Les attaquants ont utilisé des techniques avancées pour préparer la campagne, notamment l'enregistrement anticipé du domaine malveillant et la mise en place d'une copie du site légitime. Ils ont également mis en place des mesures pour limiter les téléchargements répétés, rendant l'analyse par des chercheurs plus difficile. Malgré les similarités avec la campagne de printemps, cette vague repose davantage sur l'ingénierie sociale, l'absence d'exploitation de vulnérabilités zero-day étant notable. L'APT ForumTroll, actif depuis au moins 2022, continue de cibler la Russie et la Biélorussie.

**Points Clés:**

*   **Cible:** Chercheurs et universitaires russes dans les domaines politiques et économiques.
*   **Méthode d'infection initiale:** Phishing ciblé par courriel se faisant passer pour une bibliothèque électronique.
*   **Charge utile principale:** Framework de "red teaming" commercial Tuoni, utilisé via un loader OLLVM obfusqué.
*   **Mécanisme de persistance:** COM Hijacking.
*   **Similarités avec la campagne de printemps:** Utilisation du même loader, même technique de persistance.
*   **Différences avec la campagne de printemps:** Absence d'exploitation de zero-days, utilisation de l'ingénierie sociale comme vecteur principal, framework moins rare.
*   **Durée de l'activité:** L'APT ForumTroll est actif depuis au moins 2022.

**Vulnérabilités:**

*   **CVE-2025-2783** (mentionnée dans le contexte de la campagne de printemps, pas directement dans celle décrite ici)
*   L'attaque actuelle repose sur l'ingénierie sociale plutôt que sur des vulnérabilités logicielles spécifiques, poussant les victimes à télécharger et exécuter des fichiers malveillants.

**Recommandations:**

*   Faire preuve d'une extrême vigilance face aux courriels inattendus, même s'ils semblent provenir de sources légitimes.
*   Vérifier attentivement les liens et les adresses d'expéditeurs avant de cliquer ou de télécharger des fichiers.
*   Se méfier des demandes de téléchargement de rapports ou de documents, surtout si le nom du fichier est personnalisé.
*   Sensibiliser les utilisateurs aux techniques d'ingénierie sociale et aux risques associés à l'exécution de fichiers provenant de sources non vérifiées.
*   Maintenir les logiciels de sécurité à jour et mettre en place des mesures de détection et de prévention des menaces avancées.

---
[Source](https://securelist.com/operation-forumtroll-new-targeted-campaign/118492/){:target="_blank"}
