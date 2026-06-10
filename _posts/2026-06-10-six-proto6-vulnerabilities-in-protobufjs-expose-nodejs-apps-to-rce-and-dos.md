---
title: 'Six Proto6 Vulnerabilities in protobuf.js Expose Node.js Apps to RCE and DoS'
date: 2026-06-10
permalink: /posts/2026/06/10/six-proto6-vulnerabilities-in-protobufjs-expose-nodejs-apps-to-rce-and-dos/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités Proto6 dans protobuf.js : Risques d'exécution de code à distance

La bibliothèque `protobuf.js`, largement utilisée dans les applications Node.js, les systèmes de données et les outils d'IA, est affectée par six vulnérabilités critiques (baptisées "Proto6"). Ces failles découlent d'une confiance excessive envers les schémas et métadonnées fournis en entrée, permettant à un attaquant de manipuler le comportement applicatif.

**Points clés :**
* **Impact :** Les vulnérabilités peuvent entraîner une exécution de code à distance (RCE) ou un déni de service (DoS).
* **Vecteurs d'attaque :** Manipulation de schémas, de descripteurs ou de charges utiles (payloads) malveillantes via des services Node.js, des pipelines CI/CD ou des frameworks de messagerie.
* **Mécanisme :** Le problème majeur réside dans la pollution de prototype et l'utilisation de `Function()` pour compiler des encodeurs/décodeurs, permettant l'injection de code arbitraire.

**Vulnérabilités identifiées :**
* **CVE-2026-44289 (CVSS 7.5) :** DoS par récursion protobuf illimitée.
* **CVE-2026-44290 (CVSS 7.5) :** DoS lors du chargement de schémas avec des chemins d'options non sécurisés.
* **CVE-2026-44291 (CVSS 8.1) :** Exécution de code via gadget après pollution de prototype (la plus critique).
* **CVE-2026-44292 (CVSS 5.3) :** Injection de prototype dans les constructeurs de messages.
* **CVE-2026-44294 (CVSS 5.3) :** DoS via des noms de champs contrefaits dans le code généré.
* **CVE-2026-44295 (CVSS 8.7) :** Injection de code dans la sortie statique `pbjs` via des noms de schémas contrefaits.

**Recommandations :**
* **Mise à jour immédiate :** Passer aux versions corrigées suivantes :
    * `protobuf.js` : version **7.5.6** ou **8.0.2**.
    * `protobufjs-cli` : version **1.2.1** ou **2.0.2**.
* **Bonnes pratiques :** Ne jamais considérer les schémas, métadonnées ou fichiers de configuration externes comme des entrées de confiance, particulièrement dans les environnements automatisés et les pipelines CI/CD.

---
[Source](https://thehackernews.com/2026/06/six-proto6-vulnerabilities-in.html){:target="_blank"}
