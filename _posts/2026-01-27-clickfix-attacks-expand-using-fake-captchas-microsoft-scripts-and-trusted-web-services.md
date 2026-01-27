---
title: 'ClickFix Attacks Expand Using Fake CAPTCHAs, Microsoft Scripts, and Trusted Web Services'
date: 2026-01-27
permalink: /posts/2026/01/27/clickfix-attacks-expand-using-fake-captchas-microsoft-scripts-and-trusted-web-services/
tags:
- veille-cyber
- hackernews
---
### L'évolution des attaques ClickFix : Une nouvelle menace sophistiquée

Une campagne malveillante d'envergure a été observée, baptisée ClickFix, exploitant de nouvelles techniques pour distribuer un voleur d'informations nommé Amatera. Cette attaque se démarque par son utilisation astucieuse de fausses validations CAPTCHA, combinée à des scripts Microsoft Application Virtualization (App-V) signés, afin de dissimuler l'exécution de code malveillant.

L'objectif principal de ces attaques est de tromper les utilisateurs afin qu'ils collent et exécutent une commande dans la boîte de dialogue Exécuter de Windows. Contrairement aux attaques ClickFix traditionnelles qui privilégient l'exécution directe de PowerShell, cette variante détourne le script `SyncAppvPublishingServer.vbs`, un composant légitime d'App-V. Ce script, signé numériquement et utilisé comme un binaire "living-off-the-land" (LotL), permet d'exécuter en mémoire un chargeur malveillant depuis un serveur externe, se présentant ainsi comme une alternative digne de confiance aux commandes PowerShell classiques. L'utilisation d'App-V suggère que les systèmes d'entreprise, qui en sont généralement dotés, sont les cibles privilégiées.

Le chargeur, une fois exécuté, vérifie qu'il ne tourne pas dans un environnement sandbox. Il récupère ensuite des données de configuration à partir d'un fichier Google Calendar (ICS), transformant ce service de confiance en un "dead drop resolver" pour masquer ses infrastructures et faciliter les mises à jour. Le processus se poursuit avec le décryptage et la décompression en mémoire d'un payload PowerShell, qui exécute finalement un chargeur de shellcode orchestrant le lancement d'Amatera Stealer.

Cette méthode est particulièrement insidieuse car elle repose sur l'interaction de l'utilisateur et l'abus d'outils systèmes légitimes, rendant la détection par les défenses traditionnelles complexe.

L'article met également en lumière l'évolution constante des attaques ClickFix, avec des variantes telles que JackFix, CrashFix et GlitchFix. Ces dernières exploitent diverses méthodes, allant de fausses notifications de mises à jour Windows à des pages web "glitchées" suggérant une correction. Des outils malveillants comme ErrTraffic, un système de distribution de trafic (TDS) conçu pour ces campagnes, facilitent la diffusion en injectant du JavaScript malveillant sur des sites compromis. Le phénomène est également observé dans des campagnes comme ClearFake, où des sites WordPress piratés présentent de fausses mises à jour de navigateurs pour distribuer des malwares comme Lumma Stealer, utilisant parfois des smart contracts sur la BNB Smart Chain pour dissimuler le code.

**Points clés :**

*   Nouvelle campagne ClickFix utilisant de fausses CAPTCHA pour distribuer le voleur d'informations Amatera.
*   Abus du script `SyncAppvPublishingServer.vbs` associé à Microsoft App-V pour exécuter du code malveillant en mémoire.
*   Utilisation de services de confiance comme Google Calendar pour la gestion de la configuration et de CDNs pour l'hébergement de payloads.
*   Approche "Living Off the Land" (LotL) et "Living Off the Web", exploitant des composants et workflows légitimes pour échapper à la détection.
*   Évolution des variantes ClickFix (JackFix, CrashFix, GlitchFix) et développement d'outils dédiés (ErrTraffic).
*   ClickFix est devenue une méthode d'accès initial majeure, représentant une part significative des attaques observées par Microsoft.

**Vulnérabilités / Exploitations :**

*   Abus de `SyncAppvPublishingServer.vbs` pour la télécommande d'exécution et l'évasion des défenses (associé au MITRE ATT&CK technique T1216/T1216.002).
*   Utilisation de la boîte de dialogue "Exécuter" de Windows pour inciter l'utilisateur à exécuter des commandes.
*   Technique de "dead drop resolver" utilisant des services externes comme Google Calendar pour la récupération de configuration.
*   Exécution de code en mémoire pour éviter les analyses statiques.
*   Exploitation de l'interface et des workflows de vérification familiers aux utilisateurs ("Living Off the Web").

**Recommandations :**

*   Sensibilisation accrue des utilisateurs aux techniques d'ingénierie sociale, notamment les fausses CAPTCHA et les faux messages d'erreur.
*   Surveillance des scripts `SyncAppvPublishingServer.vbs` et de leur utilisation inhabituelle, en particulier lorsqu'ils sont lancés en conjonction avec PowerShell.
*   Maintien d'un parc informatique à jour et application rigoureuse des correctifs de sécurité.
*   Mise en place de solutions de sécurité avancées capables de détecter les comportements suspects et l'exécution de code en mémoire.
*   Examen attentif des configurations et des permissions sur les systèmes d'entreprise, notamment concernant les composants App-V.
*   Filtrage des sources de trafic web suspectes et surveillance des sites potentiellement compromis.

---
[Source](https://thehackernews.com/2026/01/clickfix-attacks-expand-using-fake.html){:target="_blank"}
