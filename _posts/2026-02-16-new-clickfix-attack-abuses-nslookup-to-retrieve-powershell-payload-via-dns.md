---
title: 'New ClickFix attack abuses nslookup to retrieve PowerShell payload via DNS'
date: 2026-02-16
permalink: /posts/2026/02/16/new-clickfix-attack-abuses-nslookup-to-retrieve-powershell-payload-via-dns/
tags:
- veille-cyber
- bleepingcomp
---
**Nouvelle méthode d'attaque ClickFix : Utilisation du DNS pour la distribution de malware**

Une nouvelle technique d'attaque, baptisée ClickFix, détourne les requêtes DNS pour distribuer des charges utiles malveillantes, marquant la première utilisation connue du protocole DNS comme canal de livraison dans ce type de campagnes. Les attaques ClickFix traditionnelles incitent les utilisateurs à exécuter manuellement des commandes malveillantes, souvent sous prétexte de corriger des erreurs ou d'installer des mises koulures.

La variante découverte par Microsoft exploite la commande `nslookup` pour interroger un serveur DNS contrôlé par l'attaquant. La réponse à cette requête, contenue dans le champ "Name:", délivre un script PowerShell malveillant. Ce script est ensuite exécuté sur le système cible pour installer des logiciels malveillants supplémentaires.

L'attaque aboutit à l'installation d'un charge utile final connu sous le nom de ModeloRAT, un cheval de Troie d'accès à distance permettant aux attaquants de prendre le contrôle des systèmes compromis. Contrairement aux méthodes précédentes qui utilisaient le protocole HTTP pour la livraison, cette nouvelle approche permet aux attaquants de masquer leur trafic et de modifier leurs charges utiles dynamiquement.

Les attaques ClickFix démontrent une évolution rapide, avec des acteurs de menaces explorant diverses méthodes et types de charges utiles, y compris l'abus d'outils d'IA et le détournement de transactions de cryptomonnaies.

**Points Clés :**

*   Les attaques ClickFix évoluent pour utiliser le DNS comme canal de livraison de malware.
*   La commande `nslookup` est utilisée pour interroger un serveur DNS contrôlé par l'attaquant.
*   Le script PowerShell malveillant est contenu dans la réponse DNS.
*   Le charge utile final est le RAT ModeloRAT.
*   Cette méthode permet de masquer le trafic malveillant et de modifier les charges utiles dynamiquement.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article, l'attaque exploitant plutôt des techniques d'ingénierie sociale et des fonctionnalités existantes du système d'exploitation (commande `nslookup`, exécution PowerShell).

**Recommandations :**

*   Soyez extrêmement prudent face aux instructions demandant l'exécution de commandes dans la boîte de dialogue "Exécuter" de Windows, particulièrement celles impliquant `nslookup`.
*   Éduquez les utilisateurs sur les techniques d'ingénierie sociale et les signes d'alerte des attaques de type ClickFix.
*   Surveillez et analysez le trafic DNS pour détecter des anomalies ou des requêtes suspectes vers des serveurs inconnus.
*   Mettez en place des mesures de sécurité pour détecter et bloquer l'exécution de scripts PowerShell non autorisés.
*   Maintenez les systèmes à jour et utilisez des solutions de sécuritéEndpoint Detection and Response (EDR) pour une meilleure visibilité et capacité de réponse.

---
[Source](https://www.bleepingcomputer.com/news/security/new-clickfix-attack-abuses-nslookup-to-retrieve-powershell-payload-via-dns/){:target="_blank"}
