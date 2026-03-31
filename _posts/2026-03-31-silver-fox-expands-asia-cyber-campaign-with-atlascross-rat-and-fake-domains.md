---
title: 'Silver Fox Expands Asia Cyber Campaign with AtlasCross RAT and Fake Domains'
date: 2026-03-31
permalink: /posts/2026/03/31/silver-fox-expands-asia-cyber-campaign-with-atlascross-rat-and-fake-domains/
tags:
- veille-cyber
- hackernews
---
### Expansion de la campagne cybernétique de Silver Fox : Déploiement du RAT AtlasCross

Le groupe cybercriminel chinois **Silver Fox** (également connu sous les noms de SwimSnake, Valley Thief ou Void Arachne) intensifie ses activités en ciblant des utilisateurs russophones via des domaines de *typosquatting*. Ces sites imitent des logiciels légitimes (VPN, messageries, outils de conférence) pour diffuser une nouvelle menace sophistiquée : **AtlasCross RAT**.

#### Points clés
*   **Mode opératoire :** Utilisation de sites frauduleux pour inciter au téléchargement d'archives ZIP contenant un installateur piégé. Ce dernier déploie simultanément une application légitime (leurre) et une charge utile malveillante.
*   **Évolution technique :** AtlasCross RAT représente une montée en gamme par rapport aux outils précédents (ValleyRAT, Gh0st RAT), intégrant désormais le framework *PowerChell* pour exécuter du PowerShell en mémoire tout en contournant les protections de sécurité locales (AMSI, ETW).
*   **Infrastructure :** Le trafic C2 est chiffré via l'algorithme ChaCha20 avec des clés aléatoires.
*   **Ciblage :** La campagne vise principalement des entreprises en Asie (Japon, Inde, Philippines, Thaïlande, etc.), avec un accent particulier sur les départements financiers et managériaux.

#### Vulnérabilités et techniques d'évasion
*   **Contournement de sécurité :** Le malware neutralise activement les solutions de protection locales (360 Safe, Huorong, QQ PC Manager) au niveau TCP.
*   **Certificats volés :** Les installateurs utilisent des certificats de signature de code volés (ex: DUC FABULOUS CO.,LTD) pour paraître légitimes et tromper les systèmes de détection.
*   **Techniques :** Injection de DLL dans les processus (ex: WeChat), détournement de sessions RDP et persistance via des tâches planifiées.
*   *Note : Aucune CVE spécifique n'est mentionnée, l'attaque reposant sur l'ingénierie sociale et l'abus de légitimité plutôt que sur l'exploitation directe de failles logicielles connues.*

#### Recommandations
*   **Vérification des sources :** Télécharger uniquement des logiciels depuis les sites officiels vérifiés et se méfier des domaines aux URL légèrement modifiées (ex: `telegrtam.com.cn` au lieu de `telegram.org`).
*   **Renforcement du contrôle :** Surveiller les signatures de code des installateurs exécutés sur les postes de travail et bloquer les certificats identifiés comme compromis.
*   **Sécurité réseau :** Restreindre les communications sortantes non autorisées vers des adresses IP inconnues et surveiller les ports suspects, notamment le port TCP 9899.
*   **Sensibilisation :** Former le personnel (notamment en finance et gestion) à détecter les campagnes de phishing basées sur des thématiques courantes (fiscalité, salaires, changements de poste).
*   **Détection :** Déployer des règles EDR pour détecter l'utilisation de frameworks d'exécution PowerShell non standards et les tentatives de désactivation des fonctionnalités de journalisation de sécurité (AMSI/ETW).

---
[Source](https://thehackernews.com/2026/03/silver-fox-expands-asia-cyber-campaign.html){:target="_blank"}
