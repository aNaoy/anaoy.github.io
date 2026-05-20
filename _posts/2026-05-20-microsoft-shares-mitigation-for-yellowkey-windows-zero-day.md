---
title: 'Microsoft shares mitigation for YellowKey Windows zero-day'
date: 2026-05-20
permalink: /posts/2026/05/20/microsoft-shares-mitigation-for-yellowkey-windows-zero-day/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité YellowKey : contournement de la protection BitLocker

Microsoft a publié des mesures d'atténuation pour « YellowKey », une faille zero-day exposée par le chercheur « Nightmare Eclipse ». Cette vulnérabilité permet à un attaquant d'accéder aux données d'un lecteur chiffré par BitLocker en manipulant des fichiers spécifiques dans l'environnement de récupération Windows (WinRE).

**Points clés :**
* **Méthode d'attaque :** L'exploitation nécessite l'insertion d'un support USB contenant des fichiers « FsTx » contrefaits. En redémarrant dans WinRE et en utilisant une combinaison de touches, l'attaquant peut obtenir un accès non restreint au volume protégé.
* **Contexte :** Cette divulgation fait partie d'une série de fuites orchestrées par le chercheur en signe de protestation contre la gestion des signalements par Microsoft.

**Vulnérabilité identifiée :**
* **CVE-2026-45585 (YellowKey) :** Faille de contournement de fonctionnalité de sécurité dans Windows BitLocker.

**Recommandations de sécurité :**
* **Modification du registre :** Supprimer l'entrée `autofstx.exe` de la valeur `BootExecute` dans la clé de registre *Session Manager*. Cela empêche l'exécution automatique de l'utilitaire de récupération lors du lancement de WinRE.
* **Renforcement de l'authentification :** Passer le mode de chiffrement BitLocker de « TPM-only » à « TPM+PIN » via PowerShell, l'invite de commande ou le panneau de configuration. Cela impose la saisie d'un code PIN au démarrage, bloquant ainsi l'accès physique exploité par YellowKey.
* **Politiques de groupe :** Pour les appareils non chiffrés, configurer via Microsoft Intune ou les GPO l'option « Exiger une authentification supplémentaire au démarrage » en imposant l'utilisation d'un code PIN avec le TPM.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-shares-mitigation-for-yellowkey-windows-zero-day/){:target="_blank"}
