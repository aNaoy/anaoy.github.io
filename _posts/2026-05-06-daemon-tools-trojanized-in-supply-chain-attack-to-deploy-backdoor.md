---
title: 'DAEMON Tools trojanized in supply-chain attack to deploy backdoor'
date: 2026-05-06
permalink: /posts/2026/05/06/daemon-tools-trojanized-in-supply-chain-attack-to-deploy-backdoor/
tags:
- veille-cyber
- bleepingcomp
---
### Attaque par chaîne d'approvisionnement visant DAEMON Tools

Une campagne malveillante d'envergure, active depuis le 8 avril, a compromis les installateurs officiels du logiciel DAEMON Tools. Bien que des milliers de systèmes aient été infectés par un logiciel espion dans plus de 100 pays, l'attaque est ciblée, visant principalement des organisations sensibles (gouvernementales, scientifiques, industrielles) avec des charges utiles secondaires complexes.

**Points clés :**
*   **Vecteur d'attaque :** Distribution d'installateurs signés numériquement mais corrompus via le site officiel de DAEMON Tools.
*   **Mécanisme :** Le logiciel malveillant s'installe au démarrage, collecte des informations système (profilage) et communique avec un serveur distant.
*   **Ciblage :** Utilisation d'une porte dérobée légère pour exécuter du code à distance ; dans certains cas, déploiement du "QUIC RAT" pour une injection de code avancée.
*   **Origine suspectée :** Les indices techniques pointent vers un acteur malveillant sinophone.

**Vulnérabilités :**
*   **Versions impactées :** DAEMON Tools versions 12.5.0.2421 à 12.5.0.2434.
*   **Binaires compromis :** `DTHelper.exe`, `DiscSoftBusServiceLite.exe` et `DTShellHlp.exe`.
*   *Note : Aucune CVE n'est associée à cette attaque, il s'agit d'une compromission directe de la chaîne de compilation/distribution.*

**Recommandations :**
*   **Audit immédiat :** Examiner les machines ayant installé ou mis à jour DAEMON Tools depuis le 8 avril à la recherche de processus suspects ou d'activités réseau anormales.
*   **Surveillance :** Être vigilant face à la recrudescence des attaques par chaîne d'approvisionnement touchant des outils légitimes.
*   **Mise à jour :** Restreindre l'utilisation du logiciel dans les environnements critiques jusqu'à ce qu'une version confirmée saine soit publiée par l'éditeur.

---
[Source](https://www.bleepingcomputer.com/news/security/daemon-tools-trojanized-in-supply-chain-attack-to-deploy-backdoor/){:target="_blank"}
