---
title: 'Eight Malicious npm Packages Downloaded 40,767 Times Deliver Overlord RAT and Stealer'
date: 2026-10-07
permalink: /posts/2026/10/07/eight-malicious-npm-packages-downloaded-40767-times-deliver-overlord-rat-and-stealer/
tags:
- veille-cyber
- hackernews
---
### Campagne de malwares MALFEX sur npm : Vol de données et accès distant

Une campagne malveillante sophistiquée sur le registre npm, baptisée **MALFEX**, a été identifiée. Elle utilise des paquets JavaScript pour infecter des systèmes Windows via des scripts d'installation automatique (`postinstall hooks`). Cette campagne a totalisé plus de 40 000 téléchargements.

**Points clés :**
* **Objectif :** Déployer le cheval de Troie d'accès distant (RAT) nommé **Overlord** (écrit en Go) et des stealers Node.js capables d'exfiltrer les données de Discord, des navigateurs, de Telegram et des portefeuilles de cryptomonnaies.
* **Vecteurs d'infection :** Huit paquets malveillants identifiés (dont *function-flag*, *cdn-img-fetch* et *mxdriver*). Certains paquets agissent comme des chargeurs de code distant, tandis que d'autres utilisent des dépendances pour dissimuler l'exécution de charges utiles (`node.exe` caché dans `%APPDATA%`).
* **Attribution :** Les indices techniques (langue portugaise, fuseaux horaires) suggèrent un acteur basé au Brésil, bien que la cible soit mondiale. Le RAT Overlord est également utilisé dans d'autres campagnes exploitant des vulnérabilités WordPress.

**Vulnérabilités associées :**
* Bien que l'infection npm repose sur une ingénierie sociale et des paquets piégés, le RAT Overlord a été lié à l'exploitation des vulnérabilités suivantes :
    * **CVE-2026-63030**
    * **CVE-2026-60137**
    *(Exploits connus sous le nom de "wp2shell" affectant WordPress).*

**Recommandations :**
* **Audit des dépendances :** Vérifiez régulièrement la liste des paquets npm utilisés dans vos projets. Supprimez les paquets suspects tels que `function-flag`, `function-color`, `cdn-img-fetch`, `tlxbnhd`, `tldriver`, `mxdriver`, `img-to-native` et `native-runner`.
* **Surveillance système :** Inspectez le répertoire `%APPDATA%` à la recherche de fichiers `node.exe` suspects ou de processus inconnus s'exécutant en arrière-plan.
* **Sécurité du cycle de vie :** Désactivez ou limitez l'exécution automatique des scripts `postinstall` dans les environnements de développement et CI/CD si nécessaire, ou utilisez des outils d'analyse de composition logicielle (SCA) pour détecter les paquets malveillants connus.
* **Mise à jour :** Appliquez les correctifs pour les vulnérabilités WordPress mentionnées afin de prévenir l'injection du RAT Overlord via d'autres vecteurs.

---
[Source](https://thehackernews.com/2026/10/eight-malicious-npm-packages-downloaded.html){:target="_blank"}
