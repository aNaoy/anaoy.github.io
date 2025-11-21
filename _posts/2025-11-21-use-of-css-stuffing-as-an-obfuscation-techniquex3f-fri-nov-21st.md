---
title: 'Use of CSS stuffing as an obfuscation technique&#x3f;, (Fri, Nov 21st)'
date: 2025-11-21
permalink: /posts/2025/11/21/use-of-css-stuffing-as-an-obfuscation-techniquex3f-fri-nov-21st/
tags:
- veille-cyber
- sans-isc
---
### Utilisation de CSS pour le camouflage de contenu malveillant

Une analyse de messages de phishing a révélé une technique d'obfuscation inhabituelle utilisant le "CSS stuffing". Les attaquants ont hébergé une page de hameçonnage sur Google Firebase Storage. Bien que le code actif de la page soit relativement court (environ 10 Ko), le fichier HTML atteignait 449 Ko. La majeure partie de ce volume supplémentaire provenait de données CSS inutilisées, dont une partie était une copie modifiée du code CSS de la page, et environ un tiers était une copie de "bootstrap.min.css".

L'hypothèse avancée est que cette quantité importante de CSS, apparemment bénigne, pourrait être utilisée pour modifier le profil statistique de la page HTML afin de tromper les systèmes de sécurité basés sur des heuristiques ou de l'apprentissage automatique, et ainsi permettre au contenu malveillant de passer inaperçu. Le code contenait également l'attribut `<html lang="zxx">`, potentiellement dans le même but d'éviter une détection facile.

**Points Clés :**

*   **Technique :** "CSS stuffing" comme méthode d'obfuscation.
*   **Hébergement :** Utilisation de Google Firebase Storage, une pratique courante chez les acteurs malveillants.
*   **Objectif :** Contourner les mécanismes de filtrage de sécurité, notamment ceux basés sur l'analyse heuristique ou l'apprentissage automatique.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans cet article. L'article se concentre sur une technique d'attaque plutôt que sur une faille logicielle spécifique.

**Recommandations :**

*   Bien que l'article ne fournisse pas de recommandations directes, la nature de l'attaque suggère la nécessité d'améliorer les systèmes de sécurité pour détecter non seulement le code malveillant actif mais aussi les anomalies dans la taille et la structure des fichiers, ainsi que les métadonnées inhabituelles.
*   La surveillance des plateformes d'hébergement couramment détournées (comme Google Firebase Storage) est importante.

---
[Source](https://isc.sans.edu/diary/rss/32510){:target="_blank"}
