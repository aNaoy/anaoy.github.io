---
title: 'Russian Hackers Target Ukrainian Organizations Using Stealthy Living-Off-the-Land Tactics'
date: 2025-10-29
permalink: /posts/2025/10/29/russian-hackers-target-ukrainian-organizations-using-stealthy-living-off-the-land-tactics/
tags:
- veille-cyber
- hackernews
---
**Campagne de Cybercriminalité Russe Ciblant l'Ukraine : Discrétion et Outils Légitimes**

Des groupes de pirates informatiques d'origine russe ont mené des cyberattaques sophistiquées contre des organisations ukrainiennes, dans le but de dérober des données sensibles et de maintenir une présence persistante sur les réseaux compromis. Ces attaques, observées sur une période allant de quelques jours à deux mois, se sont distinguées par l'utilisation intensive de techniques "living-off-the-land" (LotL) et d'outils à double usage, minimisant ainsi l'emploi de logiciels malveillants conventionnels afin de rester indétectables plus longtemps.

**Points Clés :**

*   **Stratégie de Compromission :** Les attaquants ont initialement obtenu un accès aux systèmes en déployant des "web shells" sur des serveurs exposés sur Internet, probablement en exploitant des vulnérabilités non corrigées.
*   **Utilisation d'Outils LotL :** Les activités malveillantes ont largement reposé sur des outils système légitimes de Windows (comme PowerShell, RDRLeakDiag) et des applications courantes (Winbox pour la gestion de routeurs MikroTik, OpenSSH), rendant la détection plus ardue.
*   **Évasion de la Détection :** Des techniques telles que l'exclusion de répertoires des scans antivirus et la création de tâches planifiées pour des dumps mémoire ont été employées pour masquer leurs actions.
*   **Objectifs :** Vol d'informations d'identification, maintien d'un accès persistant, et potentiellement l'accès à des données sensibles comme celles stockées dans des coffres-forts de mots de passe (KeePass).
*   **Liens Potentiels avec Sandworm :** L'utilisation d'un "web shell" spécifique, LocalOlive, a été précédemment associée à un sous-groupe de l'équipe russe Sandworm. De plus, l'outil Winbox64.exe a été observé dans des campagnes antérieures ciblant l'Ukraine et attribuées à Sandworm. Bien que les analyses n'aient pas permis de confirmer un lien direct avec Sandworm dans cette campagne spécifique, l'origine russe est considérée comme probable.

**Vulnérabilités Mentionnées :**

*   **Exploitation de Vulnérabilités Non Corrigées :** Le rapport suggère que l'accès initial aux serveurs a été obtenu en exploitant une ou plusieurs vulnérabilités logicielles qui n'avaient pas été patchées.
*   **CVE-2025-8088 (WinRAR path traversal) :** Bien que distinct de la campagne LotL décrite, cet article mentionne séparément l'exploitation par le groupe Gamaredon d'une faille critique (notée 8.8 sur l'échelle CVSS) dans WinRAR pour cibler des agences gouvernementales ukrainiennes.

**Recommandations :**

*   **Mise à Jour Systématique :** Il est crucial de maintenir tous les systèmes et logiciels à jour pour corriger les vulnérabilités connues.
*   **Surveillance des Activités Système :** Renforcer la surveillance des processus et commandes système, en particulier ceux utilisant des outils légitimes de manière inhabituelle ou suspecte.
*   **Détection Basée sur le Comportement :** Mettre en place des solutions de sécurité capables de détecter les comportements anormaux plutôt que de se fier uniquement aux signatures de malwares connus.
*   **Stratégies de Défense :** L'utilisation d'une combinaison d'outils de sécurité avancés, de pratiques de sécurité rigoureuses, et d'une vigilance constante est nécessaire pour contrer les tactiques d'évasion comme celles utilisées dans ces attaques.

---
[Source](https://thehackernews.com/2025/10/russian-hackers-target-ukrainian.html){:target="_blank"}
