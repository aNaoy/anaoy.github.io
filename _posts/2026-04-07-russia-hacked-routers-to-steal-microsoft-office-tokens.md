---
title: 'Russia Hacked Routers to Steal Microsoft Office Tokens'
date: 2026-04-07
permalink: /posts/2026/04/07/russia-hacked-routers-to-steal-microsoft-office-tokens/
tags:
- veille-cyber
- krebs
---
### Espionnage par détournement DNS : la campagne Forest Blizzard

Le groupe de hackers russe "Forest Blizzard" (APT28/Fancy Bear) mène une vaste opération d'espionnage exploitant des vulnérabilités connues dans des routeurs grand public et de petites entreprises (SOHO) obsolètes. En détournant les serveurs DNS de ces appareils, les attaquants interceptent les jetons d'authentification Microsoft Office sans installer le moindre logiciel malveillant.

**Points clés**
* **Cible :** Plus de 18 000 réseaux compromis, visant principalement des institutions gouvernementales et des services de messagerie.
* **Méthode :** Utilisation du détournement DNS (DNS hijacking) pour rediriger le trafic vers des serveurs contrôlés par les attaquants, permettant des attaques "Adversary-in-the-Middle" (AiTM).
* **Impact :** Les attaquants capturent des jetons OAuth valides après l'authentification multifacteur, accédant directement aux comptes des victimes sans nécessiter de mots de passe ou de codes OTP.
* **Appareils vulnérables :** Principalement des routeurs Mikrotik et TP-Link en fin de vie ou non mis à jour.

**Vulnérabilités**
L'attaque repose sur l'exploitation de failles connues (CVE non spécifiées dans l'article, mais liées aux vulnérabilités connues des firmwares non patchés) sur les routeurs SOHO. L'absence de correctifs de sécurité permet aux attaquants de modifier les paramètres DNS par défaut.

**Recommandations**
* **Mise à jour immédiate :** Appliquer tous les correctifs de sécurité disponibles pour les routeurs. 
* **Remplacement du matériel :** Mettre hors service les routeurs obsolètes ne recevant plus de mises à jour constructeur.
* **Sécurisation des paramètres :** Vérifier les serveurs DNS configurés sur les routeurs et les appareils locaux pour s'assurer qu'ils pointent vers des résolveurs légitimes.
* **Surveillance réseau :** Surveiller les requêtes DNS suspectes et les connexions sortantes inhabituelles vers des serveurs virtuels inconnus.

---
[Source](https://krebsonsecurity.com/2026/04/russia-hacked-routers-to-steal-microsoft-office-tokens/){:target="_blank"}
