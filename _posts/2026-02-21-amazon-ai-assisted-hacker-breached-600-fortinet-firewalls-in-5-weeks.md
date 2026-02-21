---
title: 'Amazon: AI-assisted hacker breached 600 Fortinet firewalls in 5 weeks'
date: 2026-02-21
permalink: /posts/2026/02/21/amazon-ai-assisted-hacker-breached-600-fortinet-firewalls-in-5-weeks/
tags:
- veille-cyber
- bleepingcomp
---
## Amplification de l'IA dans les Cyberattaques

Une campagne malveillante, menée par un acteur russe, a exploité des services d'intelligence artificielle générative pour compromettre plus de 600 pare-feux FortiGate dans 55 pays en cinq semaines. L'attaque, survenue entre le 11 janvier et le 18 février 2026, n'a pas reposé sur des exploits de vulnérabilités connues, mais plutôt sur des interfaces de gestion exposées et des identifiants faibles sans authentification multifacteur (MFA). L'IA a été utilisée pour automatiser l'accès et l'exploration des réseaux compromis.

### Points Clés

*   **Méthode d'attaque:** Ciblage d'interfaces de gestion de pare-feux exposées sur Internet, utilisation de mots de passe faibles, et exploitation de l'IA pour automatiser les étapes post-compromission.
*   **Données extraites:** Identifiants VPN avec mots de passe récupérables, identifiants administratifs, politiques de pare-feu, configurations VPN IPsec, topologie réseau et informations de routage.
*   **Rôle de l'IA:** Génération de méthodologies d'attaque, développement de scripts personnalisés, création de cadres de reconnaissance, planification de mouvements latéraux et rédaction de documentation opérationnelle.
*   **Ciblage secondaire:** Attaques visant spécifiquement les serveurs Veeam Backup & Replication pour perturber les sauvegardes avant un éventuel déploiement de ransomware.
*   **Compétences de l'attaquant:** Qualifié de bas à moyen, mais largement amplifié par l'utilisation de l'IA, abaissant ainsi la barrière à l'entrée pour des actions complexes.

### Vulnérabilités Ciblées (ou utilisées dans les tentatives)

*   **CVE-2019-7192:** Vulnérabilité d'exécution de code à distance (RCE) sur QNAP.
*   **CVE-2023-27532:** Divulgation d'informations sur Veeam.
*   **CVE-2024-40711:** Vulnérabilité d'exécution de code à distance (RCE) sur Veeam.

Bien que l'article ne précise pas de CVE pour les pare-feux FortiGate eux-mêmes, il est indiqué que l'attaque n'a pas exploité de failles "zero-day" mais plutôt des faiblesses d'accès.

### Recommandations

*   **Ne pas exposer les interfaces de gestion** des pare-feux FortiGate à Internet.
*   **Activer l'authentification multifacteur (MFA)** pour toutes les interfaces et tous les accès.
*   **S'assurer que les mots de passe VPN diffèrent** de ceux des comptes Active Directory.
*   **Renforcer la sécurité des infrastructures de sauvegarde** pour les rendre plus résilientes aux attaques.

---
[Source](https://www.bleepingcomputer.com/news/security/amazon-ai-assisted-hacker-breached-600-fortigate-firewalls-in-5-weeks/){:target="_blank"}
