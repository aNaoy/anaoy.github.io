---
title: 'Iranian Hackers Pose as Recruiters to Deliver Cross-Platform RATs Through Coding Tests'
date: 2026-09-01
permalink: /posts/2026/09/01/iranian-hackers-pose-as-recruiters-to-deliver-cross-platform-rats-through-coding-tests/
tags:
- veille-cyber
- hackernews
---
### Espionnage cyber : Des tests de codage piégés par le groupe Nimbus Manticore

Le groupe de hackers iraniens **Nimbus Manticore** (également connu sous le nom de Mirage Kitten ou Iranian Dream Job) mène actuellement des campagnes d'espionnage ciblées en se faisant passer pour des recruteurs sur LinkedIn. Le groupe utilise de faux tests techniques pour infecter les développeurs avec des chevaux de Troie d'accès à distance (RAT) multiplateformes (Windows, Linux, macOS).

**Points clés :**
* **Vecteur d'attaque :** Envoi d'archives ZIP contenant un projet de développement nommé "Taskflow" ou des plateformes de type CTF (Capture The Flag) factices.
* **Modus Operandi :** Les attaquants demandent aux candidats de corriger des bugs dans un fichier `server.js` qui contient en réalité un package npm malveillant (`colorized_terminal` ou `pretty-log`).
* **Logiciels malveillants :**
    * **NodeRabbit :** Développé en Node.js, il communique via Azure pour exfiltrer des données, exécuter des commandes shell et maintenir une persistance persistante (tâches planifiées, entrées de registre).
    * **PollCat :** RAT en JavaScript obfusqué, conçu pour inventorier les logiciels de sécurité installés et exfiltrer des données sensibles.
* **Cibles :** Ingénieurs logiciels et professionnels de la technologie en Afrique et au Moyen-Orient.
* **Évolution :** Passage d'outils complexes en C/C++ vers des scripts multiplateformes (JavaScript/Node.js) plus discrets sur les stations de travail des développeurs.

**Vulnérabilités exploitées :**
* Aucune CVE spécifique n'est citée, car l'attaque repose sur l'ingénierie sociale : l'exécution volontaire de code non fiable par la victime et l'usage de bibliothèques npm malveillantes injectées manuellement dans le dossier `node_modules` du projet.

**Recommandations :**
* **Vigilance accrue sur le recrutement :** Se méfier des offres d'emploi reçues via les réseaux sociaux exigeant l'exécution de code localement, surtout si le processus impose une urgence artificielle ou des instructions restrictives (ex: "ne pas modifier le serveur").
* **Audit des dépendances :** Ne jamais exécuter de tests techniques contenant des packages npm non vérifiés ou des répertoires `node_modules` pré-remplis.
* **Isolation :** Exécuter les tests techniques dans des environnements isolés (machines virtuelles ou conteneurs éphémères) sans accès aux données sensibles ou au réseau local.
* **Analyse de fichiers :** Scanner systématiquement les archives reçues avec des solutions EDR/antivirus avant toute extraction ou exécution.

---
[Source](https://thehackernews.com/2026/09/iranian-hackers-pose-as-recruiters-to.html){:target="_blank"}
