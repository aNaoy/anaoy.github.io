---
title: 'Experts Reports Sharp Increase in Automated Botnet Attacks Targeting PHP Servers and IoT Devices'
date: 2025-10-29
permalink: /posts/2025/10/29/experts-reports-sharp-increase-in-automated-botnet-attacks-targeting-php-servers-and-iot-devices/
tags:
- veille-cyber
- hackernews
---
**Hausse des Attaques de Botnets Automatises : Cibles et Recommandations**

Une augmentation significative des attaques automatisées menées par des botnets tels que Mirai, Gafgyt et Mozi est constatée, ciblant spécifiquement les serveurs PHP, les appareils IoT et les passerelles cloud. Ces campagnes exploitent des vulnérabilités connues et des mauvaises configurations cloud pour étendre leur réseau. Les serveurs PHP sont particulièrement visés en raison de la popularité des systèmes de gestion de contenu comme WordPress et Craft CMS, qui présentent une large surface d'attaque due à des configurations obsolètes, des plugins et thèmes non mis à jour, et un stockage de fichiers non sécurisé.

**Points Clés :**

*   Les botnets automatisent les attaques contre les serveurs PHP, les appareils IoT et les passerelles cloud.
*   Les plateformes cloud légitimes sont utilisées pour masquer l'origine des attaques.
*   Les botnets évoluent pour offrir des services de proxy résidentiel, facilitant le trafic anonyme et les attaques.

**Vulnérabilités Exploitées :**

*   **Serveurs PHP et Frameworks :**
    *   CVE-2017-9841 : Exécution de code à distance dans PHPUnit.
    *   CVE-2021-3129 : Exécution de code à distance dans Laravel.
    *   CVE-2022-47945 : Exécution de code à distance dans le framework ThinkPHP.
    *   Utilisation de la chaîne de requête "/?XDEBUG_SESSION_START=phpstorm" pour exploiter les sessions de débogage Xdebug laissées actives en production.
*   **Appareils IoT :**
    *   CVE-2022-22947 : Exécution de code à distance dans Spring Cloud Gateway.
    *   CVE-2024-3721 : Injection de commandes dans TBK DVR-4104 et DVR-4216.
    *   Mauvaise configuration dans MVPower TV-7104HE DVR permettant l'exécution de commandes système arbitraires via une requête HTTP GET.

**Recommandations :**

*   Maintenir les appareils à jour.
*   Supprimer les outils de développement et de débogage des environnements de production.
*   Sécuriser les identifiants et clés d'API, par exemple avec AWS Secrets Manager ou HashiCorp Vault.
*   Restreindre l'accès public aux infrastructures cloud.

---
[Source](https://thehackernews.com/2025/10/experts-reports-sharp-increase-in.html){:target="_blank"}
