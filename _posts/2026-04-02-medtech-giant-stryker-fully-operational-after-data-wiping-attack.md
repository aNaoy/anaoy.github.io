---
title: 'Medtech giant Stryker fully operational after data-wiping attack'
date: 2026-04-02
permalink: /posts/2026/04/02/medtech-giant-stryker-fully-operational-after-data-wiping-attack/
tags:
- veille-cyber
- bleepingcomp
---
### Cyberattaque par effacement de données chez Stryker : rétablissement complet

Le géant des technologies médicales Stryker a annoncé un retour à une pleine capacité opérationnelle trois semaines après une cyberattaque majeure menée par le groupe hacktiviste iranien Handala. L'incident, survenu le 11 mars, a entraîné l'effacement de près de 80 000 appareils et le vol présumé de 50 téraoctets de données.

**Points clés :**
* **Nature de l'attaque :** Utilisation d'un logiciel malveillant de type « wiper » (effacement de données) et compromission d'un compte administrateur du domaine Windows.
* **Mode opératoire :** Les attaquants ont créé un nouveau compte administrateur global pour paralyser le réseau. Un fichier malveillant a été identifié a posteriori pour dissimuler leurs activités.
* **Acteurs :** Le groupe Handala, lié au ministère iranien du Renseignement et de la Sécurité (MOIS), est à l'origine de l'intrusion.
* **Conséquences :** Perturbation temporaire des capacités de production, de commande et de distribution, désormais résolue. Le FBI a depuis saisi deux sites web utilisés par le groupe.

**Vulnérabilités :**
* Compromission initiale d'un compte administrateur de domaine (Domain Admin).
* Usage abusif des privilèges de gestion via Microsoft Intune.
* Absence de détection immédiate de fichiers malveillants dissimulés dans le réseau.
* *Note : Aucune CVE spécifique n'a été attribuée à cet incident, l'attaque reposant sur l'exploitation de privilèges et des outils d'administration détournés.*

**Recommandations :**
* **Sécurisation d'Intune :** Suivre les directives de la CISA et de Microsoft pour durcir les environnements Microsoft Intune.
* **Durcissement des domaines Windows :** Appliquer les meilleures pratiques de sécurité pour limiter les privilèges d'administration et surveiller la création de comptes administrateurs globaux.
* **Veille et surveillance :** Renforcer la détection des activités anormales au sein du réseau pour identifier les outils de dissimulation utilisés par les attaquants.

---
[Source](https://www.bleepingcomputer.com/news/security/medtech-giant-stryker-fully-operational-after-data-wiping-attack/){:target="_blank"}
