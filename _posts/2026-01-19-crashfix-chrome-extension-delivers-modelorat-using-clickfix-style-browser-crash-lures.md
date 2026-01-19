---
title: 'CrashFix Chrome Extension Delivers ModeloRAT Using ClickFix-Style Browser Crash Lures'
date: 2026-01-19
permalink: /posts/2026/01/19/crashfix-chrome-extension-delivers-modelorat-using-clickfix-style-browser-crash-lures/
tags:
- veille-cyber
- hackernews
---
**Campagne CrashFix : Le Cheval de Troie ModeloRAT se Cache dans une Fausse Extension Chrome**

Une campagne de cybercriminalité, baptisée KongTuke, utilise une extension Google Chrome malveillante se faisant passer pour un bloqueur de publicités afin de déclencher volontairement des plantages du navigateur. Cette tactique vise à piéger les utilisateurs et à les inciter à exécuter des commandes arbitraires, permettant ainsi la distribution d'un nouveau cheval de Troie d'accès à distance (RAT) dénommé ModeloRAT.

Cette campagne, également connue sous le nom de CrashFix, s'appuie sur des techniques similaires à celles de ClickFix. Le système de distribution de trafic KongTuke profile d'abord les victimes avant de les rediriger vers des sites de distribution de charges utiles. Les systèmes compromis sont ensuite cédés à d'autres acteurs malveillants, notamment des groupes de rançongiciels comme Rhysida et Interlock, ainsi qu'à des acteurs comme TA866, associés à SocGholish et D3F@ck Loader.

L'attaque débute lorsqu'un utilisateur recherche un bloqueur de publicités et est redirigé, via une publicité malveillante, vers une extension sur le Chrome Web Store officiel. L'extension "NexShield – Advanced Web Guardian", qui a été téléchargée au moins 5 000 fois et n'est plus disponible, imite une extension légitime. Elle affiche un faux avertissement de sécurité indiquant que le navigateur a "cessé de fonctionner anormalement" et propose un "scan" pour résoudre une menace potentielle.

Si l'utilisateur accepte de lancer le scan, une fausse alerte de sécurité lui demande d'ouvrir la boîte de dialogue "Exécuter" de Windows, d'y coller une commande pré-copiée, puis de l'exécuter. Cette action déclenche un déni de service (DoS) en créant une boucle infinie de connexions de port runtime, épuisant les ressources du navigateur et le faisant planter.

Une fois installée, l'extension transmet un identifiant unique à un serveur contrôlé par l'attaquant (nexsnield[.]com), permettant de suivre les victimes. Le comportement malveillant est déclenché 60 minutes après l'installation et se répète toutes les 10 minutes. Le pop-up réapparaît à chaque redémarrage du navigateur après un plantage, créant une boucle d'infection. L'extension intègre également des techniques anti-analyse pour bloquer les menus contextuels et les outils de développement.

Pour exécuter la charge utile suivante, CrashFix utilise l'utilitaire légitime Windows `finger.exe` pour récupérer une commande PowerShell du serveur de l'attaquant. Ce script PowerShell, après plusieurs couches de chiffrement Base64 et d'opérations XOR, vérifie la présence d'outils d'analyse et de machines virtuelles. Si aucune analyse n'est détectée, il envoie une requête HTTP POST au serveur contenant la liste des antivirus installés et un indicateur de type de machine (domaine ou autonome).

Pour les machines jointes à un domaine, la campagne aboutit au déploiement de ModeloRAT, un RAT basé sur Python pour Windows. Ce dernier utilise le chiffrement RC4 pour les communications C2, s'assure de sa persistance via le registre, et peut exécuter des binaires, DLLs, scripts Python et commandes PowerShell. ModeloRAT peut s'auto-mettre à jour ou se terminer, et utilise une logique de "beaconing" variée pour échapper à la détection, alternant des intervalles normaux, actifs et de récupération.

Les machines autonomes font l'objet d'une séquence d'infection distincte se terminant par un message "TEST PAYLOAD!!!!" du serveur C2, suggérant que cette phase pourrait encore être en cours de test. La campagne CrashFix illustre l'évolution des tactiques d'ingénierie sociale des acteurs malveillants, exploitant la frustration des utilisateurs via un faux correctif pour leurs plantages de navigateur induits.

**Points Clés:**

*   Utilisation d'une extension Chrome malveillante ("NexShield – Advanced Web Guardian") se faisant passer pour un bloqueur de publicités.
*   Déclenchement intentionnel de plantages du navigateur pour inciter les utilisateurs à exécuter des commandes.
*   Distribution d'un nouveau RAT nommé ModeloRAT.
*   Campagne s'inscrivant dans un écosystème plus large de distribution de trafic (KongTuke).
*   Utilisation de techniques d'épuisement des ressources pour provoquer le plantage du navigateur.
*   Mise en place d'une boucle d'infection auto-entretenue.
*   Utilisation de l'utilitaire `finger.exe` pour télécharger des charges utiles.
*   Techniques d'obfuscation avancées pour la charge utile PowerShell.
*   Vérification de la présence d'outils d'analyse et de machines virtuelles.
*   Distribution différenciée des charges utiles en fonction du type de machine (domaine ou autonome).
*   Capacités avancées de ModeloRAT (exécution de code, mise à jour, persistance, beaconing adaptable).

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique (type CVE) n'est mentionnée directement concernant le logiciel victime (navigateur ou système d'exploitation). La vulnérabilité exploitée ici est comportementale et réside dans la confiance accordée par l'utilisateur à une extension malveillante et dans sa réaction face à un problème technique. L'extension elle-même exploite des fonctionnalités légitimes du navigateur pour le faire planter.

**Recommandations :**

*   **Prudence accrue avec les extensions de navigateur :** Vérifier la réputation, le nombre de téléchargements, les autorisations demandées et les avis avant d'installer une extension, même si elle provient d'une boutique officielle.
*   **Se méfier des publicités intrusives et des avertissements de sécurité non sollicités :** Les faux avertissements de sécurité sont une tactique courante des cybercriminels.
*   **Ne pas exécuter aveuglément des commandes :** Soyez extrêmement prudent avant de copier-coller et d'exécuter des commandes dans des fenêtres d'exécution ou des invites de commande, surtout si elles proviennent d'une source non vérifiée.
*   **Utiliser des logiciels de sécurité à jour :** Maintenir à jour son système d'exploitation, son navigateur et son logiciel antivirus peut aider à détecter et bloquer certaines menaces.
*   **Surveiller l'activité du navigateur :** Être attentif aux comportements inhabituels du navigateur, tels que les ralentissements soudains ou les plantages fréquents.
*   **Désinstaller les extensions suspectes :** Si une extension semble douteuse ou se comporte de manière anormale, la désinstaller immédiatement.
*   **Adopter une approche de sécurité Zero Trust :** Ne jamais faire confiance par défaut et vérifier systématiquement chaque élément, y compris les extensions et les liens.

---
[Source](https://thehackernews.com/2026/01/crashfix-chrome-extension-delivers.html){:target="_blank"}
