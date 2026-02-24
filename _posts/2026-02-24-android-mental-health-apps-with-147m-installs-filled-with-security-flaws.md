---
title: 'Android mental health apps with 14.7M installs filled with security flaws'
date: 2026-02-24
permalink: /posts/2026/02/24/android-mental-health-apps-with-147m-installs-filled-with-security-flaws/
tags:
- veille-cyber
- bleepingcomp
---
**Applications mobiles de santé mentale sur Android : des failles de sécurité exposent des données sensibles**

Une analyse de dix applications Android destinées à la santé mentale, cumulées à plus de 14,7 millions d'installations, a révélé un total de 1 575 vulnérabilités de sécurité. Ces failles pourraient potentiellement compromettre la confidentialité des utilisateurs et exposer des informations médicales très sensibles, telles que les transcriptions de thérapies, les notes de séances, les plans de médication et même des indicateurs d'automutilation. La valeur des données de thérapie sur le marché noir peut atteindre 1 000 $ ou plus par dossier, surpassant largement celle des numéros de carte de crédit.

**Points clés :**

*   Dix applications Android de santé mentale ont été examinées.
*   Un total de 1 575 vulnérabilités ont été identifiées (54 critiques, 538 modérées, 983 faibles).
*   Plus de 14,7 millions d'installations cumulées pour les applications étudiées.
*   Six des dix applications affirment que les conversations des utilisateurs restent privées ou sont chiffrées.
*   Les données de santé mentale sont particulièrement sensibles et recherchées sur le dark web.

**Vulnérabilités identifiées :**

Bien qu'aucune vulnérabilité critique n'ait été signalée de manière isolée, les failles découvertes peuvent permettre diverses attaques :

*   **Interception d'identifiants de connexion :** Permet à un attaquant d'obtenir les noms d'utilisateur et mots de passe.
*   **Usurpation de notifications :** Tromper l'utilisateur avec des alertes falsifiées.
*   **Injection HTML :** Exécution de code malveillant via des interfaces web.
*   **Géolocalisation de l'utilisateur :** Déterminer la position géographique de l'utilisateur.
*   **Accès aux activités internes non destinées à un accès externe :** Une application de thérapie a utilisé `Intent.parseUri()` sur une chaîne contrôlée par l'extérieur sans validation adéquate, permettant à un attaquant de lancer des activités internes. Ceci peut donner accès à des jetons d'authentification et des données de session, menant à la compromission des dossiers de thérapie. (Absence de CVE spécifique mentionnée dans l'article pour ce cas précis).
*   **Stockage local non sécurisé des données :** Certaines applications stockent des informations sensibles localement, les rendant lisibles par n'importe quelle autre application sur l'appareil, exposant potentiellement les détails des thérapies et les notes de séances de TCC.
*   **Données de configuration en clair :** Les ressources des fichiers APK contenaient des informations sensibles telles que les points d'accès aux API backend et une URL de base de données Firebase codée en dur.
*   **Utilisation d'une génération de nombres aléatoires cryptographiquement faible :** L'utilisation de `java.util.Random` pour générer des jetons de session ou des clés de chiffrement est considérée comme une pratique non sécurisée.
*   **Absence de détection de root :** La majorité des applications manquent de mécanismes de détection de root. Sur un appareil "jailbreaké" ou rooté, toute application disposant de privilèges root peut accéder à toutes les données de santé stockées localement.

**Recommandations :**

Les développeurs de ces applications devraient impérativement :

*   **Valider rigoureusement les entrées utilisateur :** Mettre en place une validation stricte des URI et autres données fournies par l'utilisateur pour prévenir les attaques par injection et l'accès non autorisé aux composants internes.
*   **Sécuriser le stockage des données :** Utiliser des méthodes de stockage sécurisées et chiffrées pour toutes les données sensibles stockées localement, en limitant l'accès aux applications autorisées.
*   **Éviter le stockage de données sensibles en clair :** Ne pas inclure d'informations de configuration ou d'identifiants sensibles directement dans les fichiers d'application.
*   **Utiliser des mécanismes cryptographiques robustes :** Employer des classes et des algorithmes cryptographiques sécurisés pour la génération de jetons, de clés de chiffrement et pour le chiffrement des données.
*   **Implémenter la détection de root :** Ajouter des mécanismes pour détecter si l'appareil est rooté et prendre les mesures appropriées pour protéger les données.
*   **Mettre à jour régulièrement les applications :** Assurer une maintenance et des mises à jour fréquentes pour corriger les vulnérabilités découvertes, car certaines applications n'avaient pas été mises à jour depuis des mois, voire plus d'un an.
*   **Adopter des pratiques de développement sécurisé :** Intégrer des tests de sécurité réguliers tout au long du cycle de développement pour identifier et corriger les failles avant le déploiement.

---
[Source](https://www.bleepingcomputer.com/news/security/android-mental-health-apps-with-147m-installs-filled-with-security-flaws/){:target="_blank"}
