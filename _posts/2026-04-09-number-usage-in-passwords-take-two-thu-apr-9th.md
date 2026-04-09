---
title: 'Number Usage in Passwords: Take Two, (Thu, Apr 9th)'
date: 2026-04-09
permalink: /posts/2026/04/09/number-usage-in-passwords-take-two-thu-apr-9th/
tags:
- veille-cyber
- sans-isc
---
### Analyse de l'usage des chiffres et des dates dans les mots de passe

Cette étude menée par le SANS ISC, basée sur l'analyse de près de 500 000 mots de passe capturés par des honeypots, met en lumière les habitudes prévisibles des utilisateurs et des attaquants concernant l'intégration de données temporelles dans les identifiants de connexion.

**Points clés :**
*   **Prédominance des années :** Les utilisateurs intègrent massivement l'année en cours (voire l'année suivante) dans leurs mots de passe, souvent à la fin de la chaîne de caractères.
*   **Utilisation de dates réelles :** Une part significative des mots de passe (numériques à 8 chiffres) correspond à des dates réelles (format YYYYMMDD, MMDDYYYY ou DDMMYYYY). Un grand nombre d'entre elles semblent liées à des événements récents ou à la date du jour de création du mot de passe.
*   **Comportement des bots :** Les attaquants exploitent ces tendances. Les honeypots ont révélé des tentatives d'accès utilisant des mots de passe pré-formatés avec des années futures (jusqu'en 2040), souvent pour automatiser des attaques par force brute ou des déploiements de scripts malveillants.
*   **Activité malveillante corrélée :** Certains flux de données contigus (ex: "100000") ne sont pas des mots de passe, mais des commandes ou des paramètres techniques injectés lors de tentatives de DDoS ou d'exploitation d'endpoints.

**Vulnérabilités :**
*   **Faiblesse entropique :** L'usage de motifs prévisibles (années, dates de naissance, séquences numériques comme "123") réduit drastiquement l'entropie des mots de passe, les rendant triviaux à deviner par des dictionnaires ou des attaques par force brute.
*   **Absence de CVE spécifique :** Cette problématique relève de la mauvaise hygiène de sécurité des utilisateurs et de la conception des politiques de mot de passe, plutôt que d'une faille logicielle répertoriée.

**Recommandations :**
*   **Bannir les données temporelles :** Éviter strictement d'inclure des années, des saisons, des dates de naissance ou la date actuelle dans les mots de passe.
*   **Adopter des gestionnaires de mots de passe :** Utiliser des outils générateurs de chaînes aléatoires complexes pour supprimer la composante humaine dans la création des identifiants.
*   **Renforcer l'authentification :** Implémenter systématiquement l'authentification multifacteur (MFA), qui neutralise l'efficacité des attaques par devinette de mot de passe, même lorsque ceux-ci sont prévisibles.

---
[Source](https://isc.sans.edu/diary/rss/32866){:target="_blank"}
