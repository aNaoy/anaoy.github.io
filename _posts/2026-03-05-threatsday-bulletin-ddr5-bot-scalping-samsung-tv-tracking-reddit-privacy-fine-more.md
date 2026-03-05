---
title: 'ThreatsDay Bulletin: DDR5 Bot Scalping, Samsung TV Tracking, Reddit Privacy Fine & More'
date: 2026-03-05
permalink: /posts/2026/03/05/threatsday-bulletin-ddr5-bot-scalping-samsung-tv-tracking-reddit-privacy-fine-more/
tags:
- veille-cyber
- hackernews
---
## Panorama de la Cybersécurité : Nouvelles Menaces et Évolutions Réglementaires

**Points Clés :**

*   **Campagne de Phishing Multi-Malware en Ukraine :** Des institutions gouvernementales ukrainiennes ont été ciblées par des emails de phishing contenant des archives ZIP ou des liens malveillants, distribuant les logiciels malveillants d'extraction d'informations SHADOWSNIFF et SALATSTEALER, ainsi qu'un backdoor Go nommé DEAFTICKK. Une autre campagne, potentiellement liée à APT28, utilise de nouvelles souches de malware, BadPaw et MeowMeow.
*   **Service Fictif de Gestion et de Surveillance à Distance (RMM) :** Une offre malveillante nommée TrustConnect se présente comme un outil RMM légitime, mais distribue un RAT (Remote Access Trojan) via des emails de phishing. Ce RAT permet aux attaquants de contrôler entièrement les machines infectées. Une version renommée, DocConnect, a émergé après des perturbations.
*   **Chrome Accélère ses Mises à Jour :** Google adoptera un cycle de publication bimensuel pour les nouvelles versions de Chrome, réduisant le cycle actuel de quatre semaines pour fournir plus rapidement des améliorations et des correctifs.
*   **Traçage Caché des Véhicules par TPMS :** Les capteurs des systèmes de surveillance de la pression des pneus (TPMS) émettent des signaux sans chiffrement contenant des identifiants uniques, permettant le suivi des véhicules sur de longues périodes et à distance, ouvrant la voie à des réseaux de surveillance discrets.
*   **Telegram : Un Hub pour la Cybercriminalité :** L'architecture de Telegram en fait une plateforme privilégiée pour les acteurs malveillants afin de coordonner, monétiser et promouvoir leurs opérations, remplaçant de plus en plus les écosystèmes basés sur Tor.
*   **Désorganisation de l'Infrastructure d'AuraStealer :** L'analyse de l'outil d'extraction d'informations AuraStealer a révélé 48 noms de domaine de commande et de contrôle (C2) associés à ses opérations. Cet outil, apparu après la neutralisation de Lumma Stealer, est distribué notamment via ClickFix.
*   **Malvertising Promoteur d'Atomic Stealer :** Une campagne publicitaire malveillante utilise de fausses publicités sur Google pour rediriger les utilisateurs à la recherche de solutions pour libérer de l'espace sur macOS vers des pages frauduleuses distribuant une nouvelle variante d'Atomic Stealer, nommée malext.
*   **Bots : Scalping sur le Marché de la RAM DDR5 :** Des bots effectuent un grand nombre de requêtes web scraping sur les pages de produits de mémoire vive (DRAM) pour identifier et acheter rapidement les stocks de DDR5 disponibles, dans le but de revendre ces composants à prix élevé, exacerbant les pénuries pour les consommateurs légitimes.
*   **Amende pour Reddit concernant la Protection des Données des Enfants :** Au Royaume-Uni, Reddit a été condamné à une amende de 14,47 millions de livres sterling pour le traitement illégal des données personnelles d'enfants de moins de 13 ans et pour ne pas avoir vérifié adéquatement l'âge de ses utilisateurs. Reddit a annoncé son intention de faire appel.
*   **Samsung Limite la Collecte de Données TV au Texas :** Suite à une action en justice, Samsung ne collectera plus de données ACR (Automated Content Recognition) sur ses téléviseurs intelligents sans le consentement explicite des consommateurs au Texas.
*   **Appareils Apple Approuvés par l'OTAN :** Les iPhones et iPads d'Apple sont désormais autorisés à traiter des informations classifiées au sein des réseaux de l'OTAN, devenant les premiers appareils grand public à obtenir cette approbation.
*   **TikTok Refuse le Chiffrement de Bout en Bout pour les Messagerie Directes :** TikTok ne prévoit pas d'implémenter le chiffrement de bout en bout pour ses messages directs, arguant que cela empêcherait les forces de l'ordre et les équipes de sécurité d'accéder aux messages en cas de besoin.
*   **Phishing Multi-étapes Déployant Agent Tesla :** Une nouvelle campagne de phishing utilisant des fausses commandes d'achat déploie Agent Tesla via une chaîne d'attaque complexe, incluant l'obfuscation et l'exécution en mémoire, pour voler des données sensibles tout en évitant la détection.
*   **Abus du Domaine .arpa pour le Contenu Malveillant :** Des acteurs malveillants exploitent le domaine de premier niveau .arpa, réservé à l'infrastructure réseau, pour héberger du contenu malveillant et contourner les listes de blocage traditionnelles. L'utilisation de fichiers LNK et de WebDAV est également notée pour la livraison de fichiers malveillants.
*   **Campagne de Spoofing Ciblant les Utilisateurs LastPass :** Une campagne de phishing utilise des chaînes d'emails falsifiées pour inciter les utilisateurs LastPass à visiter de fausses pages de connexion, profitant du fait que de nombreux clients de messagerie affichent le nom d'expéditeur sans révéler l'adresse réelle.
*   **Mise en Garde contre la Confiance Aveugle dans les Agents IA de Codage :** L'émergence d'outils comme Claude Code Security incite à la prudence : les IA reproduisent les schémas de code existants, y compris les faiblesses, et peuvent générer des faux positifs.
*   **LLM Permettant la Désanonymisation Automatisée sur Internet :** Des modèles de langage (LLM) ont été développés pour désanonymiser les utilisateurs d'Internet en se basant sur leurs commentaires ou indices numériques, dépassant les méthodes traditionnelles et rendant la pseudonymie moins protectrice.

**Vulnérabilités :**

*   L'article ne détaille pas de vulnérabilités spécifiques avec des identifiants CVE. Cependant, les menaces mentionnées impliquent l'exploitation de techniques de phishing, de distribution de malware (RAT, stealer, backdoors), d'abus de logiciels légitimes (RMM), de suivi via des identifiants uniques (TPMS), et de contournement des mécanismes de sécurité existants.

**Recommandations :**

*   **Vigilance face au Phishing :** Être extrêmement prudent avec les emails contenant des pièces jointes ou des liens, surtout s'ils proviennent de sources inattendues ou demandent des actions urgentes. Vérifier l'expéditeur réel.
*   **Méfiance envers les Offres Trop Belles pour être Vraies :** Être sceptique face aux outils ou services qui se présentent comme des solutions miracles, notamment ceux qui demandent un paiement pour des fonctionnalités de sécurité ou de gestion à distance.
*   **Mises à Jour Régulières :** Maintenir tous les logiciels et systèmes d'exploitation à jour pour bénéficier des derniers correctifs de sécurité.
*   **Sensibilisation à la Confidentialité :** Comprendre que de nombreux appareils connectés collectent des données. Examiner les paramètres de confidentialité et les politiques de données des services utilisés.
*   **Diversification des Outils de Sécurité :** Ne pas se fier uniquement à des solutions uniques, qu'il s'agisse de logiciels ou d'IA, pour la sécurité.
*   **Vérification Manuelle et Esprit Critique :** Ne pas déléguer aveuglément les décisions critiques à l'IA, surtout dans le domaine du développement logiciel. La validation humaine et l'esprit critique restent essentiels.
*   **Attention aux Données Publiées en Ligne :** Être conscient que les informations laissées en ligne, même sous pseudonyme, peuvent potentiellement être utilisées pour la désanonymisation.
*   **Sécurité des Comptes :** Utiliser des mots de passe forts et uniques, et envisager l'authentification multi-facteurs là où c'est possible.

---
[Source](https://thehackernews.com/2026/03/threatsday-bulletin-redis-rce-ddr5-bot.html){:target="_blank"}
