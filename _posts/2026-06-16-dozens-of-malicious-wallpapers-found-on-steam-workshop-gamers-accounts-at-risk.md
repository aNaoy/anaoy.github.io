---
title: 'Dozens of malicious wallpapers found on Steam Workshop: gamers’ accounts at risk'
date: 2026-06-16
permalink: /posts/2026/06/16/dozens-of-malicious-wallpapers-found-on-steam-workshop-gamers-accounts-at-risk/
tags:
- veille-cyber
- securelist
---
### Menace sur Steam : des fonds d'écran malveillants détournent les comptes

Des cybercriminels exploitent la fonctionnalité « application wallpaper » de l'utilitaire *Wallpaper Engine* sur Steam pour distribuer des logiciels malveillants. En publiant des contenus interactifs apparemment inoffensifs (mini-jeux, widgets), les attaquants infectent les systèmes des utilisateurs, principalement en Chine et en Russie, pour voler des identifiants Steam, déployer des backdoors (comme *DarkKomet*) ou installer des mineurs de cryptomonnaie.

**Points clés :**
* **Vecteur d'attaque :** Utilisation des « wallpapers application » qui permettent l'exécution de code arbitraire sur la machine hôte.
* **Méthodes de propagation :** Injection de fichiers malveillants dans des archives (parfois protégées par mot de passe pour contourner l'analyse) ou via des bibliothèques système corrompues (*AggregatorHost.dll*).
* **Impact :** Vol de sessions Steam actives, installation de malwares (Lumma, Vidar, RenEngine) et automatisation de la propagation via les comptes compromis.
* **Ciblage :** Majoritairement les utilisateurs chinois (89%), suivis des utilisateurs russes.

**Vulnérabilités :**
Bien qu'aucune CVE spécifique ne soit associée à cette campagne, celle-ci tire parti de la conception ouverte des « wallpapers application » de *Wallpaper Engine*, qui ne restreint pas l'exécution de programmes tiers, créant un risque de sécurité systémique.

**Recommandations :**
* **Prudence sur le Workshop :** Ne pas télécharger ou appliquer des fonds d'écran provenant de sources non vérifiées ou suspectes.
* **Analyse proactive :** Utiliser une solution antivirus/EDR à jour pour scanner les fichiers avant exécution. Les signatures de détection incluent :
    * `HEUR:Trojan-PSW.Win32.gen`
    * `HEUR:Backdoor.Win32.DarkKomet`
    * `HEUR:Trojan-Ransom.Win32.Gen.gen`
* **Vigilance accrue :** Garder à l'esprit que même des plateformes populaires peuvent être détournées pour diffuser des menaces complexes, et que la suppression par les équipes de Steam ne suffit pas à empêcher l'apparition récurrente de nouveaux contenus malveillants.

---
[Source](https://securelist.com/dozens-of-malicious-wallpapers-found-on-steam-workshop/120186/){:target="_blank"}
