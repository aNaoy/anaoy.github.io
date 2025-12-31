---
title: 'Researchers Spot Modified Shai-Hulud Worm Testing Payload on npm Registry'
date: 2025-12-31
permalink: /posts/2025/12/31/researchers-spot-modified-shai-hulud-worm-testing-payload-on-npm-registry/
tags:
- veille-cyber
- hackernews
---
## Nouvelle campagne Shai-Hulud et cheval de Troie Jackson sur Maven

Une nouvelle variante du ver Shai-Hulud a été détectée sur le registre npm, se manifestant dans le package "@vietmoney/react-big-calendar". Cette souche semble être une étape de test du chargeur utile, avec des modifications par rapport aux vagues précédentes, suggérant un accès au code source original. La campagne Shai-Hulud, apparue en septembre 2025, vise à voler des informations sensibles (clés API, identifiants cloud, jetons npm/GitHub) et utilise les jetons volés pour compromettre d'autres packages, créant un effet de ver.

Parallèlement, un package malveillant imitant la bibliothèque Jackson JSON ("org.fasterxml.jackson.core/jackson-databind") a été découvert sur Maven Central. Ce package dépose un chargeur utile Cobalt Strike après une chaîne d'attaque complexe. L'attaque exploite une vulnérabilité dans la convention de nommage Java pour créer un package ressemblant à un légitime.

### Points Clés :

*   Détection d'une nouvelle souche de Shai-Hulud sur npm, potentiellement une phase de test.
*   Shai-Hulud vole des informations sensibles et se propage de manière similaire à un ver.
*   Un package malveillant "Jackson JSON" sur Maven Central distribue un chargeur Cobalt Strike.
*   Les attaques exploitent les failles de sécurité dans les registres de packages et les noms de domaine typosquattés.

### Vulnérabilités :

*   **Shai-Hulud (npm) :** Vol d'informations sensibles (clés API, identifiants cloud, jetons npm/GitHub). L'article ne mentionne pas de CVE spécifiques pour Shai-Hulud dans cette instance.
*   **Jackson JSON (Maven) :** Exploitation de la ressemblance des noms de packages pour tromper les développeurs, permettant la livraison d'un chargeur Cobalt Strike. L'article ne mentionne pas de CVE spécifiques pour cette attaque.

### Recommandations :

*   **Pour les développeurs utilisant npm :** Examiner attentivement les dépendances, surveiller les mises à jour suspectes et utiliser des outils de sécurité pour détecter les packages malveillants.
*   **Pour les développeurs utilisant Maven :** Être vigilant face aux packages portant des noms similaires à des bibliothèques légitimes, en particulier ceux enregistrés récemment.
*   **Pour les administrateurs de registres de packages (npm, Maven Central) :** Mettre en place des mécanismes pour détecter les packages contrefaits, potentiellement en marquant les packages sous des noms de domaines similaires et en soumettant les packages à une vérification supplémentaire.

---
[Source](https://thehackernews.com/2025/12/researchers-spot-modified-shai-hulud.html){:target="_blank"}
