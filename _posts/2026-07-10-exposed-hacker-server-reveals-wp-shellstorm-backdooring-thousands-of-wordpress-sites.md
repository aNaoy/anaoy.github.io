---
title: 'Exposed Hacker Server Reveals WP-SHELLSTORM Backdooring Thousands of WordPress Sites'
date: 2026-07-10
permalink: /posts/2026/07/10/exposed-hacker-server-reveals-wp-shellstorm-backdooring-thousands-of-wordpress-sites/
tags:
- veille-cyber
- hackernews
---
### Découverte du réseau « WP-SHELLSTORM » : Une infrastructure de cybercriminalité exposée

Des chercheurs en cybersécurité ont découvert un serveur malveillant laissé sans protection, révélant le fonctionnement interne de **WP-SHELLSTORM**, un groupe spécialisé dans la compromission massive de sites WordPress et Joomla. En automatisant l'exploitation de vulnérabilités connues, le groupe a ciblé plus de 1,4 million de domaines pour y installer des portes dérobées (webshells) destinées à la revente.

#### Points clés
*   **Mode opératoire :** Le groupe utilise des scanners automatisés pour cibler des plugins obsolètes, installer des webshells (souvent basés sur « BestShell ») et maintenir un accès persistant via un malware baptisé « VShell », dissimulé sous le nom de processus système `[kworker]`.
*   **Priorité financière :** Avant de s'attaquer aux sites web, le groupe a mené une campagne contre des entreprises (fintech, e-commerce) en exploitant des serveurs de configuration Nacos pour voler des clés d'accès cloud (AWS, Alibaba, etc.).
*   **Négligence opérationnelle :** L'exposition du serveur est due à une erreur humaine (un serveur Python laissé actif sans mot de passe), permettant aux chercheurs d'analyser les listes de cibles, les journaux de commande et les outils de piratage.

#### Vulnérabilités exploitées (CVE)
Le groupe exploite principalement des failles publiques documentées :
*   **Breeze caching plugin :** CVE-2026-3844 (source principale de backdoors).
*   **Joomla JCE editor :** CVE-2026-48907 (critique et activement exploitée).
*   **Nacos :** CVE-2021-29441 (permettant le contournement de l'authentification).
*   **Autres plugins WordPress ciblés :** CVE-2026-1969 (ThemeREX), CVE-2020-36847 (Simple File List), CVE-2026-6433 (Custom CSS JS PHP), CVE-2026-0740 (Ninja Forms).

#### Recommandations
1.  **Mise à jour immédiate :** Appliquer les correctifs pour les plugins mentionnés ci-dessus (notamment Breeze 2.4.5+ et JCE 2.9.99.5+).
2.  **Audit des processus :** Vérifier les processus nommés `[kworker/X:Y]`. Si un tel processus possède un fichier exécutable, une ligne de commande ou des connexions réseau, il s'agit d'une infection par VShell.
3.  **Sécurisation Nacos :** Activer l'authentification (`nacos.core.auth.enabled=true`) et procéder à une rotation immédiate de toutes les clés et identifiants stockés dans ces instances.
4.  **Recherche de fichiers suspects :** Scanner les répertoires web à la recherche de fichiers de type `.bd.php`, `.wp-log.php` ou `.brq-*.php`.
5.  **Indicateurs de compromission (IoC) :** Bloquer les adresses IP `137.175.93.126`, `43.108.17.80` ainsi que le domaine `xs.xxooonline[.]eu[.]cc`.

---
[Source](https://thehackernews.com/2026/07/exposed-hacker-server-reveals-wp.html){:target="_blank"}
