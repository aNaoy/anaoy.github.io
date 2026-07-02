---
title: 'ConsentFix and ClickFix: How Microsoft 365 Accounts are Hijacked in 3 Seconds'
date: 2026-07-02
permalink: /posts/2026/07/02/consentfix-and-clickfix-how-microsoft-365-accounts-are-hijacked-in-3-seconds/
tags:
- veille-cyber
- bleepingcomp
---
### Détournement de comptes Microsoft 365 : Les menaces ClickFix et ConsentFix

Les cyberattaques modernes exploitent désormais les habitudes des utilisateurs plutôt que des vulnérabilités logicielles. En détournant des flux de travail courants, les attaquants compromettent des comptes Microsoft 365 en quelques secondes sans avoir besoin de deviner des mots de passe ni de contourner l'authentification multifacteur (MFA).

**Points clés**
*   **Mécanisme ClickFix :** La victime est incitée à effectuer une séquence de touches (raccourcis clavier) qui copie et exécute à son insu des commandes malveillantes sur son propre poste de travail.
*   **Mécanisme ConsentFix :** Une variante plus évoluée qui cible les flux d'autorisation OAuth de Microsoft 365. En manipulant l'utilisateur pour qu'il effectue une action spécifique (comme glisser-déposer un lien), l'attaquant intercepte les jetons de session, permettant un accès total aux emails et services sans authentification supplémentaire.
*   **Accessibilité :** Les méthodes et le code source de ces attaques sont désormais partagés ouvertement sur des forums cybercriminels, incluant des tutoriels vidéo, ce qui abaisse considérablement la barrière à l'entrée pour les attaquants.

**Vulnérabilités**
*   Il ne s'agit pas de vulnérabilités classiques (CVE), mais de l'exploitation de la **confiance humaine** combinée à des mécanismes légitimes d'authentification (OAuth) et de saisie utilisateur, détournés de leur usage prévu.

**Recommandations**
*   **Sensibilisation critique :** Former les utilisateurs à se méfier des instructions inhabituelles demandant d'utiliser des raccourcis clavier ou de déplacer des liens vers le navigateur, même dans un contexte qui semble authentique.
*   **Surveillance des points de terminaison (EDR) :** Détecter les activités anormales de PowerShell initiées par des processus utilisateur standards.
*   **Monitoring des accès :** Surveiller les nouvelles sessions de connexion provenant de localisations géographiques ou d'appareils inhabituels.
*   **Analyse du flux OAuth :** Renforcer la visibilité sur les applications tierces autorisées et les consentements accordés dans l'environnement Microsoft 365.

---
[Source](https://www.bleepingcomputer.com/news/security/consentfix-and-clickfix-how-microsoft-365-accounts-are-hijacked-in-3-seconds/){:target="_blank"}
