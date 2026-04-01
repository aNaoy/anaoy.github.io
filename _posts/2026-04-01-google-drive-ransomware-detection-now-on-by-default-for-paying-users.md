---
title: 'Google Drive ransomware detection now on by default for paying users'
date: 2026-04-01
permalink: /posts/2026/04/01/google-drive-ransomware-detection-now-on-by-default-for-paying-users/
tags:
- veille-cyber
- bleepingcomp
---
### Protection renforcée contre les ransomwares sur Google Drive

Google a généralisé sa fonctionnalité de détection de ransomwares par intelligence artificielle pour tous les utilisateurs payants de Google Workspace. Ce système, désormais activé par défaut, sécurise les fichiers stockés dans le cloud en cas d'attaque sur un poste local.

**Points clés :**
* **Mécanisme d'arrêt :** Dès la détection d'une activité suspecte lors de la synchronisation, Google Drive suspend automatiquement la synchronisation des fichiers pour éviter la propagation du chiffrement vers le cloud.
* **Efficacité accrue :** Le nouveau modèle d'IA est 14 fois plus performant que la version bêta pour identifier et bloquer les infections.
* **Alertes :** Les utilisateurs et les administrateurs informatiques reçoivent des notifications immédiates par e-mail, via l'interface Drive et dans la console d'administration.
* **Restauration :** L'outil de restauration intégré permet aux utilisateurs de récupérer rapidement les documents corrompus une fois la menace éliminée.

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée dans l'article, car il s'agit d'une mesure de protection générique contre les ransomwares ciblant les endpoints (postes de travail).

**Recommandations :**
* **Mise à jour logicielle :** Les administrateurs doivent s'assurer que Google Drive pour ordinateur est mis à jour vers la version 114 ou une version ultérieure pour bénéficier pleinement des alertes de détection.
* **Gestion des paramètres :** Bien que la fonctionnalité soit active par défaut, les administrateurs peuvent la désactiver via la console d'administration (*Apps > Google Workspace > Paramètres pour Drive et Docs > Logiciels malveillants et ransomwares*).
* **Déploiement :** Maintenir une veille sur les outils de récupération de fichiers pour assurer une réponse rapide en cas de compromission avérée sur les machines locales.

---
[Source](https://www.bleepingcomputer.com/news/security/google-drive-ransomware-detection-now-on-by-default-for-paying-users/){:target="_blank"}
