---
title: 'Russia-Aligned Hackers Abuse Viber to Target Ukrainian Military and Government'
date: 2026-01-05
permalink: /posts/2026/01/05/russia-aligned-hackers-abuse-viber-to-target-ukrainian-military-and-government/
tags:
- veille-cyber
- hackernews
---
**Utilisation de Viber par des acteurs russes pour cibler des entités ukrainiennes**

Un groupe de pirates informatiques lié à la Russie, connu sous le nom d'UAC-0184 (également désigné Hive0156), a été observé utilisant la plateforme de messagerie Viber pour mener des activités d'espionnage cybernétique contre des organisations militaires et gouvernementales ukrainiennes. Cette évolution de leurs tactiques, documentée pour la première fois en janvier 2024, s'appuie sur des précédents utilisant des applications de messagerie comme Signal et Telegram.

Les attaques débutent par l'envoi d'archives ZIP malveillantes via Viber. Ces archives contiennent des fichiers raccourcis Windows (LNK) qui, une fois ouverts par les victimes, servent de leurre tout en exécutant discrètement le malware Hijack Loader en arrière-plan. Hijack Loader est ensuite utilisé pour télécharger et déployer une deuxième archive ZIP, téléchargeant le malware via un script PowerShell.

L'attaquant déploie Hijack Loader en mémoire à l'aide de techniques visant à contourner les mesures de sécurité, telles que le "DLL side-loading" et le "module stomping". Le loader identifie également les logiciels de sécurité installés sur le système cible. Après avoir établi la persistance, généralement via des tâches planifiées, le loader injecte le RAT (Remote Access Trojan) Remcos dans le processus "chime.exe".

Remcos RAT permet aux cybercriminels de prendre le contrôle total des terminaux compromis. Ils peuvent gérer à distance l'appareil, exécuter des commandes, surveiller les activités et exfiltrer des données sensibles, facilitant ainsi des opérations d'espionnage et de vol de données à grande échelle.

**Points clés :**

*   **Acteur de menace :** UAC-0184 / Hive0156, groupe lié à la Russie.
*   **Cibles :** Entités militaires et gouvernementales ukrainiennes.
*   **Vecteur d'infection initial :** Plateforme de messagerie Viber.
*   **Charge utile primaire :** Archives ZIP contenant des fichiers LNK malveillants.
*   **Malware de premier niveau :** Hijack Loader.
*   **Malware final :** Remcos RAT.
*   **Tactic :** Utilisation de leurres (documents Office) pour masquer l'exécution du malware, techniques de contournement des antivirus, établissement de persistance, contrôle à distance et exfiltration de données.

**Vulnérabilités :**

Aucune vulnérabilité logicielle spécifique (avec CVE) n'est explicitement mentionnée dans l'article comme étant exploitée. L'attaque repose plutôt sur l'ingénierie sociale (leurres) et l'abus de fonctionnalités légitimes (Viber, PowerShell, LNK files) combinés à des techniques de contournement des défenses.

**Recommandations :**

Bien que non détaillées dans cet extrait, les actions suivantes sont généralement recommandées pour contrer ce type de menaces :

*   **Sensibilisation des utilisateurs :** Former les employés à identifier les e-mails et les messages suspects, en particulier ceux contenant des pièces jointes inattendues ou provenant de sources inconnues.
*   **Vérification des expéditeurs :** Encourager une extrême prudence lors de l'ouverture de pièces jointes ou de liens provenant de contacts non vérifiés, même via des plateformes de messagerie réputées.
*   **Mises à jour de sécurité :** Maintenir à jour les systèmes d'exploitation et les logiciels de sécurité pour bénéficier des derniers correctifs.
*   **Solutions de sécurité robustes :** Utiliser des solutions antivirus et anti-malware performantes et les maintenir à jour.
*   **Filtrage des e-mails et des messages :** Implémenter des solutions de sécurité périmétrique capables de détecter et de bloquer les malwares et les tentatives de phishing.
*   **Principes de moindre privilège :** Limiter les autorisations des utilisateurs afin de réduire l'impact potentiel d'une compromission.

---
[Source](https://thehackernews.com/2026/01/russia-aligned-hackers-abuse-viber-to.html){:target="_blank"}
