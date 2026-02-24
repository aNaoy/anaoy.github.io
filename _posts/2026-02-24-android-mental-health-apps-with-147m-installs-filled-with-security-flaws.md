---
title: 'Android mental health apps with 14.7M installs filled with security flaws'
date: 2026-02-24
permalink: /posts/2026/02/24/android-mental-health-apps-with-147m-installs-filled-with-security-flaws/
tags:
- veille-cyber
- bleepingcomp
---
## Vulnérabilités critiques dans les applications de santé mentale Android

Une analyse approfondie de dix applications Android dédiées à la santé mentale, cumulées à plus de 14,7 millions d'installations, a révélé un nombre alarmant de vulnérabilités de sécurité. Ces failles pourraient compromettre la confidentialité des données extrêmement sensibles des utilisateurs, y compris les transcriptions de thérapie, les notes de séance, et d'autres informations médicales potentiellement protégées par HIPAA. Le risque est accru par la valeur élevée de ces données sur le dark web, dépassant celle des numéros de carte de crédit.

### Points Clés :

*   **Volume des Vulnérabilités :** Au total, 1 575 vulnérabilités ont été identifiées dans les dix applications analysées, incluant 54 de gravité élevée, 538 de gravité moyenne et 983 de faible gravité.
*   **Nature des Données Compromises :** Les applications ciblent des utilisateurs souffrant de dépression clinique, d'anxiété, de troubles bipolaires, et d'autres conditions de santé mentale. Les données collectées sont donc particulièrement sensibles.
*   **Potentiel d'Exploitation :** Les vulnérabilités peuvent permettre l'interception d'identifiants de connexion, l'usurpation de notifications, l'injection HTML, la localisation d'utilisateurs, et l'accès aux enregistrements de thérapie.
*   **Faibles Mesures de Sécurité :** Certaines applications manquent de détection de racine, permettant un accès complet aux données stockées localement sur les appareils compromis. De plus, des données de configuration en clair et une utilisation d'algorithmes cryptographiques faibles ont été constatées.
*   **Mises à Jour Insuffisantes :** Une majorité des applications analysées n'avaient pas été mises à jour récemment, laissant les utilisateurs exposés aux vulnérabilités découvertes.

### Vulnérabilités Identifiées (Exemples) :

*   **Traitement Non Sécurisé des URIs :** Des applications analysent les URIs fournis par l'utilisateur sans validation adéquate, permettant l'ouverture non autorisée d'activités internes. L'utilisation de `Intent.parseUri()` sur une chaîne contrôlée extérieurement sans validation du composant cible est une cause majeure.
*   **Stockage Local Non Sécurisé des Données :** Les données sont enregistrées localement d'une manière qui accorde un accès en lecture à n'importe quelle application sur l'appareil, exposant potentiellement des détails de thérapie et des notes.
*   **Données de Configuration en Clair :** Des informations sensibles comme les points d'accès aux API backend et les URL de bases de données Firebase sont codées en dur dans les ressources des fichiers APK.
*   **Utilisation de Générateurs de Nombres Aléatoires Faibles :** L'utilisation de `java.util.Random` pour générer des jetons de session ou des clés de chiffrement est cryptographiquement peu sûre.
*   **Manque de Détection de Racine :** La plupart des applications ne disposent pas de mécanismes de détection de racine, ce qui permet à des applications malveillantes sur des appareils jailbreakés d'accéder à toutes les données de santé stockées localement.

*(Note: Les numéros CVE spécifiques ne sont pas mentionnés dans l'article.)*

### Recommandations :

*   **Développeurs d'Applications :**
    *   Implémenter une validation rigoureuse des entrées utilisateur, notamment pour les URIs.
    *   Sécuriser le stockage des données sensibles, en utilisant le chiffrement au repos.
    *   Éviter de stocker des informations de configuration sensibles ou des clés d'API en clair dans le code source ou les ressources de l'application.
    *   Utiliser des classes de génération de nombres aléatoires cryptographiquement sécurisées.
    *   Mettre en œuvre des mécanismes de détection de racine et réagir de manière appropriée si un appareil est compromis.
    *   Mettre à jour régulièrement les applications pour corriger les vulnérabilités découvertes et adoptées.
*   **Utilisateurs :**
    *   Être vigilant quant aux applications de santé mentale installées.
    *   Privilégier les applications provenant de développeurs réputés avec un historique de mises à jour de sécurité.
    *   Rester informé des mises à jour de sécurité et les appliquer rapidement.
    *   Considérer les risques liés à l'utilisation de tels outils sur des appareils avec des accès racine ou jailbreakés.

---
[Source](https://www.bleepingcomputer.com/news/security/android-mental-health-apps-with-147m-installs-filled-with-security-flaws/){:target="_blank"}
