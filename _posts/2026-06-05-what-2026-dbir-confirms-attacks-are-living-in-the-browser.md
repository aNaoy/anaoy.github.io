---
title: 'What 2026 DBIR Confirms: Attacks Are Living in the Browser'
date: 2026-06-05
permalink: /posts/2026/06/05/what-2026-dbir-confirms-attacks-are-living-in-the-browser/
tags:
- veille-cyber
- bleepingcomp
---
### L'insécurité au cœur du navigateur : Analyse du DBIR 2026

Le rapport Verizon 2026 (DBIR) met en exergue une mutation majeure de la menace cyber : le navigateur est devenu le vecteur privilégié des attaques, échappant largement aux outils de sécurité réseau et aux agents EDR traditionnels.

**Points clés :**
*   **Shadow AI :** L'usage non autorisé d'IA générative explose. 67 % des utilisateurs accèdent à ces services via des comptes personnels sur des postes professionnels, exposant des données sensibles hors du contrôle des politiques DLP (Data Loss Prevention) de l'entreprise.
*   **Angle mort du vol d'identifiants :** 39 % des brèches impliquent un abus d'identifiants. Les outils de sécurité classiques (proxys, DNS, agents endpoint) ne détectent quasiment aucune tentative de phishing moderne ou de vol de session, car celles-ci se déroulent au niveau du rendu de la page web.
*   **Risques liés aux extensions :** 13 % des extensions sont jugées critiques. 93 % des extensions malveillantes sont classées par les places de marché comme des outils de « productivité », rendant les politiques de filtrage basées sur les catégories inefficaces.
*   **Technique « ClickFix » :** Cette nouvelle forme d'ingénierie sociale manipule l'utilisateur pour qu'il exécute manuellement du code malveillant directement depuis son navigateur, facilitant l'installation de logiciels espions (infostealers).

**Vulnérabilités et menaces :**
*   L'article ne mentionne pas de CVE spécifique, car les attaques décrites exploitent le fonctionnement normal du navigateur, les comportements humains et la confiance excessive accordée aux outils de « productivité ».
*   La faille majeure réside dans le **déficit de visibilité** : les outils de sécurité ne scrutent pas l'activité interne des sessions web (exécution de scripts, interactions clavier/presse-papier, requêtes des extensions).

**Recommandations :**
*   **Déplacer la détection :** Intégrer des solutions de sécurité capables d'analyser l'activité directement dans le navigateur (Browser Security), seul endroit où l'interaction utilisateur et l'exécution du code sont visibles.
*   **Gouvernance de l'IA :** Mettre en place des alternatives d'IA gérées par l'entreprise pour limiter l'utilisation de comptes personnels.
*   **Gestion des extensions :** Abandonner le filtrage par catégorie (« productivité ») au profit d'une analyse granulaire des privilèges et des risques réels des extensions installées.
*   **Horizon de sécurité :** Considérer le navigateur non plus comme une simple application, mais comme l'environnement de travail principal nécessitant des contrôles spécifiques et isolés.

---
[Source](https://www.bleepingcomputer.com/news/security/what-2026-dbir-confirms-attacks-are-living-in-the-browser/){:target="_blank"}
