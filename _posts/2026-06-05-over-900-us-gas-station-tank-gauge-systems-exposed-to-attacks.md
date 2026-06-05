---
title: 'Over 900 US gas station tank gauge systems exposed to attacks'
date: 2026-06-05
permalink: /posts/2026/06/05/over-900-us-gas-station-tank-gauge-systems-exposed-to-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique des systèmes de contrôle de réservoirs aux États-Unis

Plus de 900 systèmes automatiques de jaugeage de réservoirs (ATG), essentiels à la surveillance des infrastructures critiques, sont actuellement exposés en ligne aux États-Unis et font l'objet d'attaques actives. Ces dispositifs, utilisés pour le contrôle des stocks de carburant et de produits chimiques, présentent des failles de sécurité majeures exploitées par des cyberacteurs pour prendre le contrôle des systèmes.

**Points clés :**
*   **Exposition massive :** Shadowserver a identifié plus de 1 000 systèmes ATG exposés mondialement, dont 909 aux États-Unis, accessibles principalement via le port TCP 10001.
*   **Risques opérationnels :** Les attaquants peuvent désactiver les alertes de sécurité, masquer des fuites réelles, fausser les relevés ou causer des dommages physiques permanents aux installations.
*   **Contexte géopolitique :** Des groupes de hackers, notamment liés à l'Iran, ont été identifiés comme responsables d'intrusions visant ces systèmes, ainsi que d'autres technologies industrielles (PLC).

**Vulnérabilités identifiées :**
L'exploitation repose sur plusieurs failles de sécurité classiques, bien que les CVE spécifiques ne soient pas détaillées dans le rapport :
*   Utilisation d'identifiants codés en dur (hardcoded credentials).
*   Absence ou faiblesse des mots de passe.
*   Contournement d'authentification.
*   Injections SQL.
*   Exécution de commandes système et élévation de privilèges.

**Recommandations de sécurité :**
*   **Isolation :** Supprimer immédiatement l'accès direct des systèmes ATG depuis l'Internet.
*   **Contrôle d'accès :** Mettre en place des pare-feu, des réseaux VPN ou des listes de contrôle d'accès (ACL) pour restreindre les connexions.
*   **Durcissement :** Remplacer systématiquement les mots de passe par défaut par des identifiants robustes.
*   **Maintenance :** Appliquer les mises à jour de sécurité dès leur disponibilité.
*   **Surveillance :** Implémenter l'authentification multifacteur (MFA) si possible et surveiller activement les journaux pour détecter toute modification non autorisée.

---
[Source](https://www.bleepingcomputer.com/news/security/over-900-us-gas-station-tank-gauge-systems-exposed-to-attacks/){:target="_blank"}
