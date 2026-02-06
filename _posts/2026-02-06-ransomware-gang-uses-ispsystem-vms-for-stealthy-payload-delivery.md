---
title: 'Ransomware gang uses ISPsystem VMs for stealthy payload delivery'
date: 2026-02-06
permalink: /posts/2026/02/06/ransomware-gang-uses-ispsystem-vms-for-stealthy-payload-delivery/
tags:
- veille-cyber
- bleepingcomp
---
### Exploitation de machines virtuelles pour la diffusion de rançongiciels

Des groupes de cybercriminels exploitent les machines virtuelles (VM) provisionnées par ISPsystem, un fournisseur légitime d'infrastructure virtuelle, pour héberger et diffuser à grande échelle des charges utiles malveillantes. Les chercheurs de Sophos ont découvert que ces acteurs utilisent des VM Windows avec des noms d'hôte identiques, suggérant l'utilisation de modèles par défaut générés par la plateforme VMmanager d'ISPsystem.

Cette vulnérabilité permet aux opérateurs de rançongiciels, y compris LockBit, Qilin, Conti, BlackCat/ALPHV, ainsi qu'aux campagnes impliquant les voleurs d'informations RedLine et Lummar, de dissimuler leurs systèmes malveillants parmi des milliers d'autres systèmes légitimes. Cette tactique complique l'attribution des attaques et retarde la neutralisation des infrastructures compromises. Les VM malveillantes sont souvent hébergées par des fournisseurs de "bulletproof hosting" réputés pour leur manque de coopération avec les autorités.

ISPsystem, suite à ces découvertes, a confirmé avoir mis à jour VMmanager pour introduire la randomisation des noms d'hôte lors du déploiement de nouvelles VM Windows, résolvant ainsi le problème d'identification technique uniforme.

**Points Clés :**

*   Des groupes de rançongiciels et de malwares utilisent des VM provisionnées via ISPsystem pour la diffusion de leurs charges utiles.
*   La faiblesse réside dans l'utilisation de modèles par défaut par VMmanager d'ISPsystem, générant des noms d'hôte identiques.
*   Cette méthode permet de masquer les infrastructures malveillantes, de compliquer l'attribution et de rendre les neutralisations plus difficiles.
*   Des fournisseurs d'hébergement peu scrupuleux sont impliqués dans cette exploitation.
*   ISPsystem a corrigé la vulnérabilité en implémentant la génération aléatoire des noms d'hôte.

**Vulnérabilités :**

*   Les modèles par défaut de VMmanager d'ISPsystem génèrent des noms d'hôte et des identifiants système identiques pour les VM Windows déployées. Il n'y a pas de CVE spécifique référencé pour cette vulnérabilité dans l'article.

**Recommandations :**

*   Pour ISPsystem : Implémenter la génération aléatoire des noms d'hôte pour les VM afin d'éviter les identifiants dupliqués.
*   Pour les fournisseurs d'hébergement : Renforcer la diligence raisonnable et refuser de fournir des services à des acteurs malveillants.
*   Pour les équipes de sécurité : Être vigilant quant à l'utilisation d'infrastructures d'hébergement potentiellement compromises et surveiller la présence de VM avec des identifiants inhabituels ou des modèles par défaut.

---
[Source](https://www.bleepingcomputer.com/news/security/ransomware-gang-uses-ispsystem-vms-for-stealthy-payload-delivery/){:target="_blank"}
