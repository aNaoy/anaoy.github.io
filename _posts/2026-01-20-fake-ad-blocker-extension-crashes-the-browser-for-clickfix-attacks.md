---
title: 'Fake ad blocker extension crashes the browser for ClickFix attacks'
date: 2026-01-20
permalink: /posts/2026/01/20/fake-ad-blocker-extension-crashes-the-browser-for-clickfix-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Extension Malveillante et Attaques "CrashFix"

Une campagne de malvertising utilise une fausse extension de blocage de publicités pour Chrome et Edge, nommée NexShield. Cette extension provoque intentionnellement des plantages du navigateur afin de faciliter des attaques de type "ClickFix", rebaptisées "CrashFix" par les chercheurs. L'objectif final est de déployer des outils d'accès à distance, tels que ModeloRAT, dans des environnements d'entreprise.

**Points Clés :**

*   **NexShield :** Une fausse extension présentée comme un bloqueur de publicités légitime, promue par un faux nom et exploitant la confiance associée à des projets connus. Elle a été retirée du Chrome Web Store.
*   **Mécanisme de Crash :** L'extension crée une boucle infinie de connexions de ports "chrome.runtime", épuisant les ressources mémoire du navigateur. Cela entraîne des gels, une utilisation accrue du CPU et de la RAM, menant à un crash du navigateur.
*   **Ingénierie Sociale Post-Crash :** Après le redémarrage du navigateur, une fausse alerte de sécurité s'affiche, incitant l'utilisateur à lancer un scan pour "corriger" le problème.
*   **Attaque ClickFix ("CrashFix") :** L'extension copie une commande malveillante dans le presse-papiers de l'utilisateur. L'utilisateur est alors invité à la coller et l'exécuter via l'invite de commande, déclenchant ainsi un script PowerShell obfusqué et potentiellement le téléchargement d'autres charges utiles.
*   **Payload :** Un script PowerShell avec un délai d'exécution de 60 minutes après l'installation de NexShield est utilisé pour éviter la détection. Pour les hôtes d'entreprise, le RAT Modelo est déployé, permettant la reconnaissance, l'exécution de commandes, la modification du registre et l'introduction de nouvelles charges utiles. Pour les utilisateurs domestiques, un message "TEST PAYLOAD!!!!" a été observé, suggérant une priorité plus faible ou un travail en cours.
*   **Acteur de la Menace :** L'attaque CrashFix est attribuée à un acteur nommé "KongTuke", qui semble évoluer et cibler davantage les réseaux d'entreprise.

**Vulnérabilités :**

*   Aucune vulnérabilité logicielle spécifique (CVE) n'est mentionnée dans l'article. L'attaque repose sur l'installation d'une extension malveillante par l'utilisateur et l'exploitation de sa confiance.

**Recommandations :**

*   **Prudence avec les extensions :** Installer des extensions uniquement à partir de sources et d'éditeurs de confiance.
*   **Comprendre les commandes :** S'assurer de comprendre l'impact de toute commande externe exécutée sur le système.
*   **Nettoyage complet :** Si l'extension NexShield a été installée, il est impératif d'effectuer un nettoyage complet du système, car la désinstallation de l'extension ne suffit pas à supprimer toutes les charges utiles malveillantes.

---
[Source](https://www.bleepingcomputer.com/news/security/fake-ad-blocker-extension-crashes-the-browser-for-clickfix-attacks/){:target="_blank"}
