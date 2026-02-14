---
title: 'One threat actor responsible for 83% of recent Ivanti RCE attacks'
date: 2026-02-14
permalink: /posts/2026/02/14/one-threat-actor-responsible-for-83-of-recent-ivanti-rce-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Acteur Unique Responsable de la Majorité des Exploitations Ivanti

Un acteur malveillant unique est à l'origine de plus de 83% des attaques exploitant activement deux vulnérabilités critiques dans Ivanti Endpoint Manager Mobile (EPMM). Ces failles, permettant l'exécution de code à distance sans authentification, ont été exploitées en "zero-day". L'infrastructure de cet acteur, hébergée par PROSPERO OOO (AS200593), est également utilisée pour cibler d'autres produits, notamment Oracle WebLogic, GNU Inetutils Telnetd et GLPI.

**Points Clés :**

*   Un seul acteur est responsable de 83% des exploitations actives des vulnérabilités Ivanti EPMM.
*   Ces attaques visaient deux vulnérabilités critiques dans Ivanti EPMM.
*   L'acteur utilise une infrastructure "bulletproof".
*   L'activité d'exploitation est fortement automatisée et utilise divers user agents.
*   Les attaques utilisent souvent des "callbacks" DNS pour vérifier l'exécution des commandes, suggérant une activité d'intermédiaire d'accès initial.
*   L'adresse IP dominante n'est pas toujours présente dans les listes publiques d'indicateurs de compromission (IoC).

**Vulnérabilités (avec CVE) :**

*   **CVE-2026-21962:** Vulnérabilité critique dans Ivanti EPMM permettant l'exécution de code à distance.
*   **CVE-2026-24061:** Vulnérabilité critique dans Ivanti EPMM permettant l'exécution de code à distance.
*   CVE-2026-1281 (mentionnée comme corrigée par des hotfixes, mais des correctifs permanents sont attendus).
*   CVE-2026-1340 (mentionnée comme corrigée par des hotfixes, mais des correctifs permanents sont attendus).
*   CVE-2026-21962: Vulnérabilité dans Oracle WebLogic (le même identifiant CVE est mentionné pour deux produits différents dans l'article, cela pourrait être une erreur ou une confusion dans le texte source).
*   CVE-2026-24061: Vulnérabilité dans GNU Inetutils Telnetd (le même identifiant CVE est mentionné pour deux produits différents dans l'article, cela pourrait être une erreur ou une confusion dans le texte source).
*   CVE-2025-24799: Vulnérabilité dans GLPI.

**Recommandations :**

*   Appliquer les hotfixes fournis par Ivanti.
*   Pour les versions EPMM 12.5.0.x, 12.6.0.x, et 12.7.0.x, utiliser les packages RPM 12.x.0.x.
*   Pour les versions EPMM 12.5.1.0 et 12.6.1.0, utiliser les packages RPM 12.x.1.x.
*   Il est recommandé de reconstruire une instance EPMM de remplacement et d'y migrer toutes les données pour une approche plus conservatrice.
*   Bloquer l'adresse IP 193[.]24[.]123[.]42, qui est la source dominante des attaques et qui n'est pas toujours répertoriée dans les listes d'IoC publiques.

---
[Source](https://www.bleepingcomputer.com/news/security/one-threat-actor-responsible-for-83-percent-of-recent-ivanti-rce-attacks/){:target="_blank"}
