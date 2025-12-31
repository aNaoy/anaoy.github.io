---
title: 'New ErrTraffic service enables ClickFix attacks via fake browser glitches'
date: 2025-12-31
permalink: /posts/2025/12/31/new-errtraffic-service-enables-clickfix-attacks-via-fake-browser-glitches/
tags:
- veille-cyber
- bleepingcomp
---
### ErrTraffic : Automatisation des Attaques ClickFix par Faux Glitchs de Navigateur

Un nouvel outil criminel nommé ErrTraffic permet aux acteurs malveillants d'automatiser les attaques de type ClickFix. Il génère de faux "glitchs" sur des sites web compromis pour inciter les victimes à télécharger des charges utiles ou à suivre des instructions malveillantes. Cette plateforme promet des taux de conversion élevés et peut adapter les charges utiles au système cible.

Le ClickFix est une technique d'ingénierie sociale qui trompe les cibles en leur faisant exécuter des commandes dangereuses sous des prétextes crédibles, tels que la correction de problèmes techniques ou la validation d'identité. Cette méthode gagne en popularité, notamment auprès des cybercriminels et des acteurs étatiques, pour son efficacité à contourner les contrôles de sécurité standards.

ErrTraffic, promu sur des forums de piratage russophones, est vendu sous forme de système de distribution de trafic auto-hébergé pour 800 $. Il offre une interface conviviale avec des options de configuration et des données de campagne en temps réel. L'attaquant doit préalablement contrôler un site web ou y avoir injecté du code malveillant.

Lorsque les critères de ciblage (géolocalisation, système d'exploitation) sont remplis pour un visiteur, ErrTraffic modifie l'interface du site pour simuler des dysfonctionnements visuels tels que du texte corrompu, des remplacements de polices, de fausses mises à jour Chrome ou des erreurs de police système. Ces faux problèmes servent de prétexte pour proposer une "solution", comme l'installation d'une mise à jour de navigateur, le téléchargement d'une police système, ou la copie d'une commande dans l'invite de commandes.

Si la victime suit les instructions, un script JavaScript ajoute une commande PowerShell au presse-papiers. Son exécution entraîne le téléchargement d'une charge utile, pouvant inclure des voleurs d'informations comme Lumma et Vidar pour Windows, le trojan Cerberus pour Android, AMOS pour macOS, ou des backdoors non spécifiées pour Linux. Les clients d'ErrTraffic peuvent spécifier les charges utiles par architecture et les pays ciblés, avec une exclusion notable des pays de la CEI. Les données volées sont ensuite vendues sur des marchés du dark web ou utilisées pour compromettre d'autres sites.

**Points Clés :**

*   **ErrTraffic :** Plateforme automatisant les attaques ClickFix.
*   **Mécanisme :** Création de faux "glitchs" sur des sites web pour tromper les utilisateurs.
*   **Objectif :** Inciter les victimes à exécuter des commandes ou télécharger des charges utiles malveillantes.
*   **Popularité du ClickFix :** Méthode d'ingénierie sociale efficace et adoptée par divers acteurs.
*   **Fonctionnalités :** Interface utilisateur, ciblage géographique et OS, personnalisation des charges utiles.
*   **Charges Utiles :** Voleurs d'informations (Lumma, Vidar, AMOS), trojans (Cerberus), backdoors Linux.
*   **Commercialisation :** Vente à l'unité pour 800 $ sur des forums de piratage.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article, l'attaque reposant sur l'ingénierie sociale et l'exécution de commandes par l'utilisateur.

**Recommandations :**

*   **Prudence accrue :** Méfiance face aux messages d'erreur inhabituels ou aux demandes de mise à jour non sollicitées sur des sites web.
*   **Vérification des instructions :** Ne pas exécuter aveuglément des commandes ou des scripts, surtout s'ils sont copiés depuis un navigateur.
*   **Mises à jour manuelles :** Obtenir les mises à jour logicielles ou les correctifs directement depuis les sites officiels des éditeurs.
*   **Sensibilisation à la sécurité :** Former les utilisateurs aux techniques d'ingénierie sociale et aux risques associés à l'exécution de commandes inconnues.
*   **Sécurité des sites web :** Les propriétaires de sites doivent surveiller et sécuriser leurs plateformes contre les injections de code malveillant.

---
[Source](https://www.bleepingcomputer.com/news/security/new-errtraffic-service-enables-clickfix-attacks-via-fake-browser-glitches/){:target="_blank"}
