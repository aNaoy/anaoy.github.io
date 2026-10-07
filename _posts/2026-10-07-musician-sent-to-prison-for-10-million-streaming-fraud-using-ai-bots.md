---
title: 'Musician sent to prison for $10 million streaming fraud using AI bots'
date: 2026-10-07
permalink: /posts/2026/10/07/musician-sent-to-prison-for-10-million-streaming-fraud-using-ai-bots/
tags:
- veille-cyber
- bleepingcomp
---
### Condamnation pour fraude massive aux redevances de streaming par IA

Un musicien américain, Michael Smith, a été condamné à 18 mois de prison pour avoir orchestré une fraude aux redevances de streaming d'un montant de 10 millions de dollars. Entre 2017 et 2024, il a inondé les plateformes (Spotify, Apple Music, etc.) de centaines de milliers de titres générés par intelligence artificielle, diffusés en boucle par des réseaux de bots automatisés.

**Points clés :**
* **Méthode :** Utilisation de plus de 1 000 comptes de bots automatisés pour générer des milliards d'écoutes artificielles.
* **Contournement :** Utilisation massive de VPN pour masquer l'origine des connexions et échapper aux systèmes de détection de fraude.
* **Échelle :** À son apogée, le système générait plus de 660 000 écoutes par jour. Smith a accumulé plus de 12 millions de dollars de revenus frauduleux depuis 2019.
* **Impact :** Détournement massif de revenus au détriment des artistes légitimes et falsification des statistiques de popularité.
* **Sanction :** 18 mois de prison, deux ans de liberté surveillée et plus de 8 millions de dollars à rembourser au titre de la confiscation des avoirs.

**Vulnérabilités exploitées :**
L'affaire ne repose pas sur une vulnérabilité logicielle (CVE) spécifique, mais sur une **faille systémique des plateformes de streaming** : l'incapacité initiale de leurs algorithmes de détection à distinguer un comportement humain légitime d'une activité automatisée à grande échelle, même lorsque celle-ci utilise des proxys (VPN).

**Recommandations :**
* **Analyse comportementale avancée :** Renforcer les systèmes de détection pour identifier les schémas d'écoute non humains (fréquence, durée, corrélation temporelle).
* **Vérification de l'identité :** Durcir les processus de création de comptes et de validation des abonnements (notamment pour les comptes "famille" utilisés pour amplifier le volume d'écoutes).
* **Audit des contenus :** Mettre en œuvre des outils de filtrage pour détecter et signaler les contenus générés par IA massivement produits sans valeur artistique réelle.
* **Surveillance réseau :** Détecter et limiter le trafic provenant de services VPN ou de centres de données connus, souvent utilisés pour masquer des activités malveillantes.

---
[Source](https://www.bleepingcomputer.com/news/security/musician-gets-18-months-in-prison-for-10-million-streaming-fraud-using-ai-bots/){:target="_blank"}
