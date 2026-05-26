---
title: 'Microsoft Defender can now automatically isolate hacked endpoints'
date: 2026-05-26
permalink: /posts/2026/05/26/microsoft-defender-can-now-automatically-isolate-hacked-endpoints/
tags:
- veille-cyber
- bleepingcomp
---
### Isolation automatique des terminaux compromis par Microsoft Defender

Microsoft déploie une nouvelle fonctionnalité en mode « preview » pour *Microsoft Defender for Endpoint* : l’isolement automatique des terminaux suspects. Ce mécanisme s'intègre à la stratégie de disruption automatique des attaques afin de stopper la progression des menaces au sein du réseau.

**Points clés :**
* **Fonctionnement :** Lorsqu'un terminal est identifié comme compromis, Defender coupe ses communications réseau pour empêcher les mouvements latéraux, l'exfiltration de données ou la propagation de rançongiciels.
* **Maintien de la visibilité :** Le terminal isolé reste connecté au service *Microsoft Defender* pour permettre aux équipes de sécurité de poursuivre la surveillance et l'analyse.
* **Portée :** La fonctionnalité concerne exclusivement les stations de travail sous Windows intégrées (onboarded) et gérées par *Defender for Endpoint*.
* **Contrôle humain :** Les administrateurs conservent la main pour libérer manuellement un terminal de son isolement une fois l'incident traité.

**Vulnérabilités :**
* Aucun CVE spécifique n'est mentionné. L'article se concentre sur une solution proactive visant à limiter l'impact des attaques par mouvements latéraux (latéral movement) et des attaques de type « hands-on-keyboard ».

**Recommandations :**
* **Activation :** Tester la fonctionnalité de disruption automatique dans les environnements de pré-production via le portail *Microsoft Defender*.
* **Gestion des incidents :** Former les équipes de réponse sur incident à identifier les terminaux isolés via le menu « Device inventory » afin de pouvoir lever l'isolement une fois la remédiation effectuée.
* **Extension de la protection :** S'assurer que tous les actifs critiques sont correctement intégrés à *Defender for Endpoint* pour bénéficier de cette capacité de confinement automatisé.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-defender-can-now-automatically-isolate-hacked-endpoints/){:target="_blank"}
