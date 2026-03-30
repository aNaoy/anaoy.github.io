---
title: 'Apple adds macOS Terminal warning to block ClickFix attacks'
date: 2026-03-30
permalink: /posts/2026/03/30/apple-adds-macos-terminal-warning-to-block-clickfix-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Sécurisation renforcée du Terminal macOS contre les attaques ClickFix

Apple a introduit dans macOS Tahoe 26.4 un mécanisme de sécurité visant à contrer les attaques de type « ClickFix ». Cette fonctionnalité détecte le collage de commandes potentiellement malveillantes dans le Terminal et interrompt leur exécution pour afficher une mise en garde explicite à l'utilisateur.

**Points clés :**
* **Nature de l'attaque :** Le « ClickFix » est une technique d'ingénierie sociale incitant les utilisateurs à copier-coller des commandes malveillantes dans leur terminal, souvent sous prétexte de résoudre un problème technique.
* **Fonctionnement du correctif :** Le système analyse le contenu collé (notamment depuis Safari) et, en cas de risque suspecté, bloque l'exécution immédiate tout en informant l'utilisateur des dangers potentiels.
* **Limites actuelles :** Le dispositif semble fonctionner par session. Les critères précis d'analyse de dangerosité ne sont pas officiellement documentés par Apple, et certains tests suggèrent que l'alerte ne se déclenche pas systématiquement après la première exécution.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée à cette mise à jour, car il s'agit d'une mesure préventive contre une technique d'ingénierie sociale (exploitation de l'utilisateur plutôt qu'une faille logicielle directe).

**Recommandations :**
* **Méfiance systématique :** Ne jamais exécuter de commandes trouvées sur Internet si vous ne comprenez pas précisément leur fonctionnement et leurs conséquences.
* **Ne pas se reposer uniquement sur les protections natives :** L'alerte macOS ne constitue pas une protection infaillible ; elle ne dispense pas l'utilisateur de vérifier la provenance et la légitimité des instructions qu'il manipule.
* **Prudence lors des collages :** Si vous recevez un avertissement du système, considérez-le comme un signal sérieux pour abandonner l'opération.

---
[Source](https://www.bleepingcomputer.com/news/security/apple-adds-macos-terminal-warning-to-block-clickfix-attacks/){:target="_blank"}
