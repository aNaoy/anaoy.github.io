---
title: '144 Mastra npm Packages Compromised via Hijacked Contributor Account'
date: 2026-06-17
permalink: /posts/2026/06/17/144-mastra-npm-packages-compromised-via-hijacked-contributor-account/
tags:
- veille-cyber
- hackernews
---
### Compromission massive de la chaîne d'approvisionnement via les paquets npm Mastra

Une attaque par chaîne d'approvisionnement a compromis 144 paquets npm du framework Mastra. L'incident a été rendu possible par le piratage du compte d'un ancien contributeur, permettant aux attaquants de publier des versions malveillantes en contournant les flux de publication sécurisés.

**Points clés :**
* **Mécanisme :** L'attaque utilise une dépendance contrefaite nommée `easy-day-js` (clone malveillant de la bibliothèque `dayjs`) ajoutée aux paquets.
* **Exécution :** La charge utile s'exécute automatiquement via un hook `postinstall` lors de l'installation du paquet, avant même que le code ne soit importé ou utilisé.
* **Charge utile :** Un cheval de Troie multiplateforme capable de voler des données de navigateurs et de portefeuilles de cryptomonnaies, d'assurer sa persistance sur le système et de télécharger des modules distants.
* **Portée :** Le paquet `@mastra/core`, très utilisé, a été infecté, exposant potentiellement un grand nombre d'environnements de développement et CI/CD.

**Vulnérabilités :**
* **Absence de signature obligatoire :** Le projet Mastra permettait la publication via des jetons npm personnels sans exiger systématiquement une preuve de provenance (attestations SLSA).
* **Accès non révoqué :** Le maintien des droits d'accès d'un ancien contributeur (compte "ehindero") a facilité l'intrusion.
* **CVE :** Aucune CVE spécifique n'a été attribuée à cet incident au moment de l'analyse, celui-ci relevant d'une exploitation malveillante plutôt que d'une faille de code logicielle classique.

**Recommandations :**
* **Audit de sécurité :** Examiner les environnements (workstations, runners CI) ayant installé ces versions pour détecter des traces d'activité suspecte ou de persistance.
* **Rotation des secrets :** Considérer comme compromis tous les identifiants, clés API ou jetons présents sur les machines ayant installé les paquets infectés.
* **Renforcement de la publication :** Imposer des politiques de sécurité strictes, telles que la vérification obligatoire des signatures et des attestations de provenance pour chaque paquet.
* **Gestion des accès :** Appliquer le principe du moindre privilège en révoquant systématiquement l'accès aux dépôts et au registre npm pour tout contributeur quittant un projet.

---
[Source](https://thehackernews.com/2026/06/144-mastra-npm-packages-compromised-via.html){:target="_blank"}
