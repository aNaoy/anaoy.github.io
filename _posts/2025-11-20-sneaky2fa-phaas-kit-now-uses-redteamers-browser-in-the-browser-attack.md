---
title: 'Sneaky2FA PhaaS kit now uses redteamers Browser-in-the-Browser attack'
date: 2025-11-20
permalink: /posts/2025/11/20/sneaky2fa-phaas-kit-now-uses-redteamers-browser-in-the-browser-attack/
tags:
- veille-cyber
- bleepingcomp
---
### Usurpation d'Identité Renforcée : Le Kit Phishing "Sneaky2FA" Exploite une Technique de Fausses Fenêtres

Le kit de phishing-as-a-service (PhaaS) Sneaky2FA a intégré une technique nommée "Browser-in-the-Browser" (BitB) pour mieux subtiliser les identifiants et les sessions actives d'utilisateurs Microsoft. Ce nouveau stratagème vient s'ajouter à ses méthodes précédentes, notamment l'utilisation d'images SVG pour les attaques et les tactiques d'attaquant-en-le-milieu (AitM) qui permettent de contourner l'authentification à deux facteurs (2FA).

Le principe du BitB consiste à présenter à la victime une fausse fenêtre de connexion, imitant parfaitement une authentification légitime, y compris l'apparence de l'URL dans la barre d'adresse. Cette fausse fenêtre est intégrée à la page de phishing via un "iframe" et s'adapte visuellement au système d'exploitation et au navigateur de la cible pour un réalisme accru.

Lorsqu'un utilisateur clique sur un lien piégé, il est d'abord confronté à un contrôle de sécurité (Cloudflare Turnstile dans cet exemple), puis invité à se connecter avec son compte Microsoft pour accéder à un contenu. En choisissant cette option, une fenêtre BitB s'ouvre, affichant un formulaire de connexion Microsoft trompeur.

Le kit utilise ensuite le système AitM pour intercepter les identifiants et, surtout, les jetons de session valides qui sont transmis à la page de phishing. Ces informations permettent aux attaquants de se connecter au compte de la victime, même si la 2FA est activée, car ils exploitent une session déjà authentifiée.

Les pages de phishing de Sneaky2FA sont conçues pour être furtives, utilisant un code JavaScript et HTML obfusqué pour échapper à la détection par les outils de sécurité. Elles redirigent les robots et les chercheurs vers des pages inoffensives.

**Points clés :**

*   **Évolution des techniques de phishing :** Sneaky2FA, un kit PhaaS populaire, adopte la technique BitB pour améliorer l'efficacité de ses attaques.
*   **Contournement de la 2FA :** L'intégration du BitB avec les capacités AitM permet de voler des identifiants et des sessions actives, rendant la 2FA inopérante.
*   **Mimétisme réaliste :** Les fausses fenêtres de connexion BitB sont conçues pour être indistinguables des fenêtres légitimes, incluant une barre d'adresse trompeuse.
*   **Évasion des défenses :** Les pages de phishing sont obfusquées pour éviter la détection par les outils de sécurité statiques.

**Vulnérabilités exploitées :**

Bien qu'aucun CVE spécifique ne soit mentionné dans l'article, la technique exploitée cible la confiance des utilisateurs dans les interfaces de connexion légitimes et la manière dont les services authentifient les sessions via des jetons. La vulnérabilité réside dans la capacité des attaquants à tromper l'utilisateur pour qu'il interagisse avec une fausse interface d'authentification qui transmet des informations sensibles.

**Recommandations :**

*   **Vérification attentive des fenêtres de connexion :** Soyez particulièrement vigilant face aux fenêtres de connexion qui apparaissent subitement, même si elles semblent légitimes. Essayez de les déplacer en dehors de la fenêtre principale de votre navigateur ; une fausse fenêtre restera intégrée.
*   **Examen de la barre d'adresse :** Vérifiez toujours l'URL affichée dans la barre d'adresse du navigateur. Les fausses fenêtres BitB peuvent présenter une URL correcte, mais elle fait partie d'un "iframe".
*   **Méfiance face aux demandes de connexion inattendues :** Ne cliquez pas sur des liens provenant de sources non fiables, même s'ils promettent des documents ou des accès importants. Accédez directement aux services légitimes en tapant leur adresse dans votre navigateur.
*   **Sensibilisation aux techniques de phishing :** Comprendre comment fonctionnent les techniques comme le BitB peut aider à les identifier.
*   **Utilisation de solutions de sécurité à jour :** Maintenez vos logiciels antivirus et anti-malware à jour et utilisez des extensions de navigateur qui signalent les sites suspects.

---
[Source](https://www.bleepingcomputer.com/news/security/sneaky2fa-phaas-kit-now-uses-redteamers-browser-in-the-browser-attack/){:target="_blank"}
