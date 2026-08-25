---
title: 'Hackers breached over 270 Zimbra servers in ongoing attacks'
date: 2026-08-25
permalink: /posts/2026/08/25/hackers-breached-over-270-zimbra-servers-in-ongoing-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Vague de compromissions critiques sur les serveurs Zimbra

Plus de 270 instances de Zimbra Collaboration Suite (ZCS) ont été compromises par des attaquants exploitant une faille de sécurité activement utilisée. Cette vulnérabilité permet une exécution de code à distance (RCE) sans authentification, ciblant le composant de surveillance SNMP.

**Points clés :**
*   **Vulnérabilité exploitée :** CVE-2026-73570 (injection de commande via le composant SNMP activé).
*   **Impact :** Plus de 270 serveurs confirmés comme compromis ; plus de 8 200 instances vulnérables ont été identifiées à travers le monde.
*   **Réponse officielle :** La CISA a intégré cette faille à son catalogue KEV et a imposé un correctif urgent aux agences fédérales américaines.

**Recommandations :**
*   **Mise à jour :** Appliquer immédiatement la version ZCS 10.1.20 ou supérieure, qui corrige cette vulnérabilité.
*   **Audit des journaux :** Rechercher des activités suspectes, notamment des redémarrages inattendus du service Zimbra.
*   **Inspection des fichiers :** Vérifier la présence de fichiers suspects créés au cours des 30 derniers jours dans les répertoires `/opt/zimbra/jetty/webapps/`, `/opt/zimbra/jetty_base/webapps/` et `/tmp/`.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-breached-over-270-zimbra-servers-in-ongoing-attacks/){:target="_blank"}
