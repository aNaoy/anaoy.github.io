---
title: 'Hackers Hid Vasilek Backdoor in VMware Tools During 2-Year Russian Healthcare Intrusion'
date: 2026-10-21
permalink: /posts/2026/10/21/hackers-hid-vasilek-backdoor-in-vmware-tools-during-2-year-russian-healthcare-intrusion/
tags:
- veille-cyber
- hackernews
---
### Intrusion persistante et backdoor Vasilek : Analyse du groupe Partisan Zmiy

Le groupe de hacktivistes « Partisan Zmiy » (Cyber Partisans) a infiltré une organisation de santé russe pendant près de deux ans, privilégiant l'espionnage à long terme plutôt que la destruction immédiate.

**Points clés :**
*   **Persistance furtive :** Les attaquants ont utilisé un service nommé `vmauad` masqué en composant VMware légitime. Ils ont détourné le répertoire de VMware Tools pour implanter des binaires malveillants ou remplacer des DLL légitimes (notamment `vmtools.dll`).
*   **Backdoor Vasilek (v1.5.8) :** Cet outil permet une prise de contrôle totale : exécution de commandes, capture d'écran, enregistrement de frappes clavier, exfiltration de données et simulation d'entrées utilisateur (souris).
*   **Command & Control (C2) :** Utilise Telegram pour le pilotage (actuellement instable en Russie) et des tunnels GOST programmés hebdomadairement.
*   **Évolution des méthodes :** Contrairement à leurs attaques destructrices habituelles (wiper *Pryanik*), le groupe a ici maintenu une présence silencieuse pour exploiter les relations de confiance de l'infrastructure cible.
*   **Autres menaces identifiées :** Le rapport souligne également la circulation du cheval de Troie *HypeAgent*, capable de dérober des cookies de sessions (Discord, Binance, GitHub, etc.) et de manipuler des portefeuilles cryptographiques.

**Vulnérabilités exploitées :**
*   **Hijacking de processus (DLL Side-loading) :** Remplacement de composants légitimes de VMware par des versions malveillantes dans des répertoires non surveillés.
*   **Défaut de surveillance :** Utilisation prolongée de services système (Windows services) non audités pour maintenir la persistance.
*   *(Note : Aucune CVE spécifique n'est mentionnée pour ces techniques, il s'agit d'abus de fonctionnalités légitimes et de faiblesses de configuration).*

**Recommandations de sécurité :**
*   **Audit des répertoires systèmes :** Surveiller les répertoires d'installation des logiciels tiers (type `C:\Program Files\VMware\VMware Tools\`) pour détecter tout ajout ou remplacement non autorisé de fichiers DLL ou exécutables.
*   **Surveillance des services Windows :** Auditer les services créés récemment ou masqués sous des noms de fournisseurs légitimes (ex: `vmauad`).
*   **Contrôle des flux sortants :** Restreindre les communications vers les services de messagerie utilisés comme C2 (Telegram) si ces outils ne sont pas nécessaires à l'activité métier.
*   **Gestion des accès :** Appliquer le principe du moindre privilège, particulièrement pour les services système, afin d'empêcher l'élévation de privilèges via `runas`.
*   **Analyse comportementale :** Détecter les anomalies de comportement, comme des tunnels réseaux établis à des fréquences inhabituelles (hebdomadaires) ou des simulations de saisie utilisateur suspectes.

---
[Source](https://thehackernews.com/2026/10/hackers-hid-vasilek-backdoor-in-vmware.html){:target="_blank"}
