---
title: 'EtherRAT Distribution Spoofing Administrative Tools via GitHub Facades'
date: 2026-04-30
permalink: /posts/2026/04/30/etherrat-distribution-spoofing-administrative-tools-via-github-facades/
tags:
- veille-cyber
- hackernews
---
### Campagne EtherRAT : Ciblage des administrateurs via des outils usurpés

Une campagne malveillante sophistiquée, active depuis fin 2025, cible les administrateurs système, les ingénieurs DevOps et les analystes en cybersécurité. En usurpant des outils d'administration légitimes (tels que PsExec, Sysmon, LAPS ou Kusto Explorer), les attaquants s'assurent d'infecter des postes disposant de privilèges élevés pour faciliter des mouvements latéraux au sein des réseaux d'entreprise.

**Points clés de l'attaque :**
*   **Distribution via GitHub :** Utilisation d'une architecture à deux niveaux. Un premier dépôt "façade" est optimisé pour le SEO (empoisonnement des résultats de recherche) afin de tromper les victimes, tandis qu'un second dépôt distinct héberge le malware (MSI).
*   **Infrastructure résiliente (EtherHiding) :** Le malware utilise la blockchain Ethereum comme mécanisme de "Dead Drop Resolving" (DDR). Au lieu de contacter un serveur C2 en dur, le logiciel interroge des contrats intelligents pour obtenir dynamiquement l'adresse de son infrastructure de commande, rendant les blocages IP ou DNS inefficaces.
*   **Profilage et persistance :** Le malware est un cheval de Troie d'accès à distance (RAT) basé sur Node.js, capable d'exécuter des commandes arbitraires. Il dissimule son activité en s'exécutant via `conhost.exe --headless`.
*   **Acteurs potentiels :** Des recherches suggèrent un lien technique entre EtherRAT, le groupe Lazarus (Corée du Nord) et le malware Tsundere (lié à MuddyWater/Iran).

**Vulnérabilités :**
*   L'article ne mentionne pas de CVE spécifique, car l'attaque repose sur l'ingénierie sociale (téléchargement d'outils malveillants) et l'abus de fonctionnalités système légitimes pour maintenir la persistance.

**Recommandations :**
*   **Sécurité réseau :** Bloquer l'accès aux points de terminaison RPC publics d'Ethereum utilisés par le malware pour résoudre ses adresses C2.
*   **Gestion des outils :** Obliger le téléchargement d'outils d'administration exclusivement via des portails officiels, vérifiés et sécurisés, et proscrire le téléchargement depuis des résultats de moteurs de recherche.
*   **Chasse aux menaces (Threat Hunting) :**
    *   Surveiller les processus `node.exe` exécutant des commandes shell ou les instances de `conhost.exe` avec l'argument `--headless`.
    *   Identifier les requêtes sortantes répétitives (toutes les 5 minutes) vers des passerelles RPC Ethereum.
    *   Analyser les logs historiques pour détecter des communications avec des domaines C2 suspects ou des nœuds blockchain.

---
[Source](https://thehackernews.com/2026/04/etherrat-distribution-spoofing.html){:target="_blank"}
