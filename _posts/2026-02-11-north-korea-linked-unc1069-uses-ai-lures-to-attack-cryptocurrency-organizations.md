---
title: 'North Korea-Linked UNC1069 Uses AI Lures to Attack Cryptocurrency Organizations'
date: 2026-02-11
permalink: /posts/2026/02/11/north-korea-linked-unc1069-uses-ai-lures-to-attack-cryptocurrency-organizations/
tags:
- veille-cyber
- hackernews
---
**UNC1069 : L'IA au Service du Cyberdétournement d'Actifs Numériques**

Un groupe de cybercriminels nord-coréen, connu sous le nom d'UNC1069, cible activement le secteur des cryptomonnaies. Leur objectif est de dérober des données sensibles sur les systèmes Windows et macOS afin de réaliser des transactions financières frauduleuses.

Les tactiques employées reposent sur une ingénierie sociale sophistiquée. Elles incluent l'utilisation de comptes Telegram compromis, de fausses invitations à des réunions Zoom et l'exploitation du vecteur d'infection ClickFix. Une nouveauté marquante est l'utilisation de vidéos générées par intelligence artificielle (IA), y compris des deepfakes, pour tromper les victimes. L'IA est également mobilisée pour créer des contenus d'hameçonnage et même pour développer des codes malveillants destinés à subtiliser des cryptomonnaies.

UNC1069, actif depuis au moins avril 2018, est également identifié sous les pseudonymes CryptoCore et MASAN. Le groupe a recentré ses attaques depuis 2023, passant des techniques de spear-phishing traditionnelles à des cibles dans l'écosystème Web3, telles que les plateformes d'échange centralisées (CEX), les développeurs logiciels dans les institutions financières et les entreprises de haute technologie, ainsi que les individus travaillant dans des fonds de capital-risque.

Lors de leurs récentes incursions, les attaquants ont déployé jusqu'à sept familles de logiciels malveillants distinctes, dont plusieurs nouvelles telles que SILENCELIFT, DEEPBREATH et CHROMEPUSH.

Le déroulement typique d'une attaque :
1.  **Prise de contact :** Le groupe approche les victimes via Telegram en se faisant passer pour des capital-risqueurs ou en utilisant des comptes compromis d'entrepreneurs légitimes.
2.  **Invitation à une réunion :** Une réunion est planifiée via Calendly. Le lien de la réunion redirige vers un faux site web imitant Zoom.
3.  **Phishing vidéo :** Une fois sur le faux site, les victimes sont invitées à activer leur caméra et à entrer leur nom, pensant participer à une réunion Zoom réelle. Des vidéos préenregistrées ou des deepfakes sont diffusées pour maintenir l'illusion d'un appel en direct.
4.  **Injection de malware :** Un faux message d'erreur concernant un problème audio incite la victime à télécharger et exécuter une commande de dépannage. Sur macOS, cela conduit à l'exécution d'un script qui dépose un binaire malveillant.

**Points Clés :**

*   **Acteur de menace :** UNC1069 (également connu sous les noms de CryptoCore et MASAN).
*   **Cible principale :** Organisations et individus dans le secteur des cryptomonnaies et Web3.
*   **Techniques :** Ingénierie sociale, spear-phishing, utilisation de comptes compromis, fausses invitations à des réunions.
*   **Outils d'attaquant :** Intelligence artificielle (IA) générative pour les leurres et le développement de code, deepfakes, ClickFix, malwares divers.
*   **Objectif final :** Vol de données sensibles et détournement financier.

**Vulnérabilités Exploités (non spécifiées par CVE) :**

*   **Confiance dans les plateformes de communication :** Exploitation de la familiarité avec Zoom et Telegram.
*   **Manque de vigilance face aux contenus générés par IA :** Les deepfakes et autres vidéos synthétiques trompent les utilisateurs.
*   **Faiblesse de la validation des liens et des téléchargements :** Les victimes sont amenées à cliquer sur des URL malveillantes et à exécuter des fichiers suspects.
*   **Exploitation des bases de données de contrôle d'accès :** Le malware DEEPBREATH manipule la base de données TCC de macOS pour obtenir un accès aux fichiers sensibles.

**Logiciels Malveillants Identifiés :**

*   **BIGMACHO :** Backdoor distribué sous couvert d'un kit de développement logiciel (SDK) Zoom.
*   **SILENCELIFT :** Backdoor minimaliste envoyant des informations système à un serveur C2.
*   **DEEPBREATH :** Malware pour macOS, capable de voler des identifiants (iCloud Keychain, navigateurs, Telegram, Notes) et d'accéder aux données via la manipulation de TCC.
*   **CHROMEPUSH :** Extension de navigateur pour Chrome et Brave, déguisée en outil d'édition hors ligne de Google Docs, capable de voler des cookies, d'enregistrer les frappes et de capturer les identifiants et mots de passe.
*   **WAVESHAPER :** Exécutable C++ collectant des informations système et déployant le downloader HYPERCALL.
*   **HYPERCALL :** Downloader en Go servant à distribuer d'autres charges utiles.
*   **HIDDENCALL :** Backdoor en Go offrant un accès au système compromis.
*   **SUGARLOADER :** Downloader en C++ déployant CHROMEPUSH.

**Recommandations :**

*   **Prudence accrue face aux communications non sollicitées :** Vérifier rigoureusement l'expéditeur et le contenu des messages, en particulier lorsqu'ils proviennent de plateformes comme Telegram.
*   **Suspicion face aux invitations à des réunions :** Valider la légitimité des réunions et des organisateurs, préférer les plateformes de communication officielles et sécurisées.
*   **Vigilance face aux contenus multimédias :** Se méfier des vidéos et des images qui semblent trop parfaites ou inhabituelles, notamment celles prétendument générées par IA ou deepfakes.
*   **Ne jamais télécharger ou exécuter de logiciels provenant de sources non fiables :** S'assurer que les logiciels sont téléchargés depuis les sites officiels des éditeurs.
*   **Renforcer la sécurité des systèmes :** Maintenir les systèmes d'exploitation et les logiciels à jour, utiliser des solutions antivirus et anti-malware robustes, et configurer correctement les paramètres de sécurité (comme le contrôle d'accès aux applications).
*   **Sensibilisation continue :** Former régulièrement les employés aux risques de phishing, d'ingénierie sociale et aux tactiques d'attaquants émergentes.
*   **Authentification forte :** Utiliser l'authentification multi-facteurs (MFA) partout où cela est possible.

---
[Source](https://thehackernews.com/2026/02/north-korea-linked-unc1069-uses-ai.html){:target="_blank"}
