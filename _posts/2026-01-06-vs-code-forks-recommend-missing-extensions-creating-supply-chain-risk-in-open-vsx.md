---
title: 'VS Code Forks Recommend Missing Extensions, Creating Supply Chain Risk in Open VSX'
date: 2026-01-06
permalink: /posts/2026/01/06/vs-code-forks-recommend-missing-extensions-creating-supply-chain-risk-in-open-vsx/
tags:
- veille-cyber
- hackernews
---
**Extensions Fantômes : Un Risque Invisible pour la Chaîne d'Approvisionnement Logicielle**

Des versions modifiées de Visual Studio Code (VS Code), telles que Cursor, Windsurf, Google Antigravity et Trae, recommandent des extensions qui n'existent pas dans le registre Open VSX. Cette situation crée une faille potentielle dans la chaîne d'approvisionnement logicielle, car des acteurs malveillants peuvent s'approprier les noms de ces extensions inexistantes et y publier des paquets dangereux.

Ces environnements de développement intégrés (IDE) héritent de la liste des extensions recommandées par le marché officiel de Microsoft. Or, ces extensions n'étant pas répertoriées sur Open VSX, leurs espaces de noms sont libres. N'importe qui peut donc enregistrer ces noms et y charger des logiciels malveillants.

Lorsqu'un développeur utilise l'un de ces IDE modifiés et qu'une notification propose d'installer une extension recommandée (par exemple, pour PostgreSQL s'il a le programme installé), il peut tomber dans le piège. L'IDE suggère une extension qui n'existe pas officiellement mais dont le nom est désormais occupé par une version malveillante sur Open VSX. Une simple action d'installation peut alors compromettre le système du développeur, entraînant le vol d'identifiants, de secrets ou de code source. Il a été constaté que des extensions fictives ont été installées plusieurs centaines de fois, simplement parce qu'elles étaient proposées comme recommandations.

Parmi les noms d'extensions dont les espaces de noms ont été réclamés par des chercheurs pour démontrer le risque, on trouve :
*   ms-ossdata.vscode-postgresql
*   ms-azure-devops.azure-pipelines
*   msazurermtools.azurerm-vscode-tools
*   usqlextpublisher.usql-vscode-ext
*   cake-build.cake-vscode
*   pkosta2005.heroku-command

Suite à ces découvertes, Cursor, Windsurf et Google ont déployé des correctifs. La fondation Eclipse, qui gère Open VSX, a retiré les contributeurs non officiels et mis en place des mesures de sécurité accrues au niveau du registre.

**Points Clés :**

*   Des forks de VS Code recommandent des extensions inexistantes sur Open VSX.
*   Les acteurs malveillants peuvent s'approprier ces noms pour distribuer des logiciels malveillants.
*   Le risque concerne la chaîne d'approvisionnement logicielle et peut mener au vol de données sensibles.

**Vulnérabilités :**

*   Aucune CVE spécifique n'est mentionnée dans l'article pour cette vulnérabilité. Le problème réside dans la gestion des espaces de noms d'extensions non répertoriées.

**Recommandations :**

*   Les développeurs doivent faire preuve de prudence avant d'installer des extensions, même recommandées.
*   Vérifier systématiquement la source et l'éditeur des extensions proposées.
*   Les projets utilisant des forks de VS Code devraient auditer leurs recommandations d'extensions pour s'assurer de leur validité.

---
[Source](https://thehackernews.com/2026/01/vs-code-forks-recommend-missing.html){:target="_blank"}
