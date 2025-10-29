---
title: 'Qilin ransomware abuses WSL to run Linux encryptors in Windows'
date: 2025-10-29
permalink: /posts/2025/10/29/qilin-ransomware-abuses-wsl-to-run-linux-encryptors-in-windows/
tags:
- veille-cyber
- bleepingcomp
---
**Qilin : Une nouvelle tactique pour échapper aux défenses**

Les opérateurs du rançongiciel Qilin ont recours à une méthode innovante pour déjouer les mesures de sécurité traditionnelles. Ils exploitent le Sous-système Windows pour Linux (WSL) afin d'exécuter des versions Linux de leur rançongiciel directement sur des systèmes Windows. Cette approche leur permet d'éviter la détection par les logiciels de sécurité orientés vers les menaces Windows classiques.

Le groupe Qilin, précédemment connu sous le nom d'Agenda, est particulièrement actif, ayant ciblé plus de 700 victimes réparties dans 62 pays cette année. Les affiliés de Qilin utilisent une combinaison d'outils légitimes (AnyDesk, ScreenConnect, Splashtop pour l'accès à distance, Cyberduck et WinRAR pour le vol de données) et d'utilitaires intégrés à Windows (Paint, Notepad) pour identifier et exfiltrer des informations sensibles.

Une technique notable observée est l'utilisation de pilotes vulnérables (BYOVD) pour désactiver les logiciels de sécurité. Les attaquants déploient des pilotes signés mais vulnérables, comme eskle.sys, afin de stopper les processus antivirus et EDR. Ils emploient également le DLL sideloading pour charger des pilotes du noyau (rwdrv.sys, hlpdrv.sys) conférant des privilèges élevés. Des outils tels que "dark-kill" et "HRSword" sont également utilisés pour neutraliser les défenses et effacer les traces de leurs activités.

La particularité réside dans l'utilisation du WSL. Les rançongiciels Linux de Qilin sont des exécutables ELF qui ne peuvent pas fonctionner nativement sous Windows. Cependant, en activant ou en installant le WSL sur un système compromis, les attaquants créent un environnement Linux capable d'exécuter ces binaires. Cela permet au rançongiciel de s'exécuter sans être détecté par les mécanismes de sécurité Windows focalisés sur le comportement des malwares natifs. Cette adaptation souligne la capacité des acteurs de menaces à exploiter les environnements hybrides pour maximiser leur portée et contourner les défenses.

**Points clés :**

*   Utilisation du Sous-système Windows pour Linux (WSL) pour exécuter des rançongiciels Linux sur Windows.
*   Technique permettant d'échapper aux solutions de sécurité traditionnelles axées sur les malwares Windows.
*   Utilisation d'outils légitimes et d'utilitaires Windows pour la reconnaissance et le vol de données.
*   Recours à des pilotes vulnérables (BYOVD) pour désactiver les logiciels de sécurité.
*   Le groupe Qilin est une menace active avec un grand nombre de victimes à l'échelle mondiale.

**Vulnérabilités (CVE) :**

*   Aucune vulnérabilité spécifique avec identifiant CVE n'est explicitement mentionnée dans l'article concernant la méthode d'exploitation du WSL ou l'utilisation de pilotes vulnérables. L'accent est mis sur la technique d'attaque globale plutôt que sur une faille logicielle précise.

**Recommandations :**

*   **Surveillance des activités WSL :** Mettre en place une surveillance accrue des activités liées à l'installation et à l'utilisation du Sous-système Windows pour Linux (WSL) sur les postes de travail et serveurs Windows.
*   **Gestion des privilèges :** Appliquer une politique de moindre privilège pour limiter la capacité des utilisateurs et des processus à installer ou activer des fonctionnalités système telles que WSL.
*   **Sécurité des pilotes :** Renforcer la politique de sécurité concernant le chargement de pilotes, en privilégiant les listes blanches et en auditant l'utilisation de pilotes non signés ou potentiellement vulnérables.
*   **Détection avancée :** Investir dans des solutions de sécurité capables de détecter le comportement malveillant au sein des environnements virtuels ou conteneurisés, y compris ceux créés par WSL.
*   **Sensibilisation des utilisateurs :** Informer les utilisateurs sur les risques liés à l'accès à distance et au téléchargement de logiciels suspects.
*   **Mises à jour et correctifs :** Maintenir tous les systèmes d'exploitation et logiciels à jour pour atténuer les vulnérabilités connues.

---
[Source](https://www.bleepingcomputer.com/news/security/qilin-ransomware-abuses-wsl-to-run-linux-encryptors-in-windows/){:target="_blank"}
