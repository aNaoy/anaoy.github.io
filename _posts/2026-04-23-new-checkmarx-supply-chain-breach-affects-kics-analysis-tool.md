---
title: 'New Checkmarx supply-chain breach affects KICS analysis tool'
date: 2026-04-23
permalink: /posts/2026/04/23/new-checkmarx-supply-chain-breach-affects-kics-analysis-tool/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de la chaîne d'approvisionnement de l'outil Checkmarx KICS

Des attaquants ont compromis les images Docker et les extensions VSCode/Open VSX de l'outil d'analyse open-source **KICS** (Keeping Infrastructure as Code Secure). Cette attaque par chaîne d'approvisionnement visait à exfiltrer des données sensibles directement depuis les environnements des développeurs.

**Points clés :**
* **Méthodologie :** Les pirates ont injecté un composant malveillant ("MCP addon") téléchargeant un script (`mcpAddon.js`) capable de voler des identifiants.
* **Cibles de l'exfiltration :** Jetons GitHub, clés SSH, identifiants cloud (AWS, Azure, Google Cloud), jetons npm, variables d'environnement et configurations locales.
* **Exfiltration :** Les données volées étaient chiffrées et envoyées vers le domaine malveillant `audit.checkmarx[.]cx`. Les attaquants utilisaient également des dépôts GitHub publics pour stocker les données exfiltrées.
* **Période d'exposition :** La compromission des images Docker a eu lieu le 22 avril 2026 entre 14:17 et 15:41 UTC.

**Vulnérabilités :**
* Aucune CVE spécifique n'a été attribuée, l'incident résultant d'une compromission directe des dépôts officiels et des processus de distribution.

**Recommandations :**
* **Rotation des secrets :** Considérer comme compromis tous les identifiants, tokens et clés SSH présents sur les systèmes ayant utilisé KICS le 22 avril 2026.
* **Mise à jour :** Revenir aux versions saines confirmées :
    * DockerHub KICS : **v2.1.20**
    * Checkmarx ast-github-action : **v2.3.36**
    * Checkmarx VS Code extensions : **v2.64.0**
    * Checkmarx Developer Assist : **v1.18.0**
* **Blocage réseau :** Bloquer les adresses IP liées aux domaines malveillants :
    * `91.195.240.123` (checkmarx.cx)
    * `94.154.172.43` (audit.checkmarx.cx)
* **Bonnes pratiques :** Privilégier l'utilisation de SHA (hachages) plutôt que des tags pour le pull d'images Docker afin d'éviter le remplacement par des versions non vérifiées.

---
[Source](https://www.bleepingcomputer.com/news/security/new-checkmarx-supply-chain-breach-affects-kics-analysis-tool/){:target="_blank"}
