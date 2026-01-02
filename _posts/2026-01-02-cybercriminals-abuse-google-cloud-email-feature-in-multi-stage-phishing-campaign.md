---
title: 'Cybercriminals Abuse Google Cloud Email Feature in Multi-Stage Phishing Campaign'
date: 2026-01-02
permalink: /posts/2026/01/02/cybercriminals-abuse-google-cloud-email-feature-in-multi-stage-phishing-campaign/
tags:
- veille-cyber
- hackernews
---
**Campagne d'hameçonnage sophistiquée exploitant Google Cloud**

Une campagne d'hameçonnage multicanal a été découverte, exploitant la fonction d'envoi d'e-mails du service Google Cloud Application Integration pour diffuser des messages malveillants. Les attaquants usurpent l'identité de notifications légitimes de Google (telles que des alertes de messagerie vocale ou des demandes d'accès à des fichiers) envoyées depuis une adresse de confiance ("noreply-application-integration@google[.]com") afin de contourner les filtres de sécurité traditionnels.

Plus de 9 000 e-mails auraient été envoyés à environ 3 200 clients dans le monde, touchant divers secteurs, dont la fabrication, la technologie, la finance et le commerce de détail. Les messages frauduleux imitent le style et la structure des notifications Google pour gagner la confiance des destinataires.

Le processus d'attaque implique plusieurs étapes de redirection. Après avoir cliqué sur un lien dans l'e-mail, l'utilisateur est dirigé vers un service Google Cloud légitime, puis vers un autre domaine Google pour une vérification type CAPTCHA, conçue pour déjouer les outils de sécurité automatisés. Finalement, les victimes sont conduites vers une fausse page de connexion Microsoft hébergée sur un domaine non-Microsoft, où leurs identifiants sont dérobés.

**Points Clés :**

*   **Exploitation d'une fonctionnalité légitime :** Les attaquants utilisent la fonction "Send Email" de Google Cloud Application Integration pour envoyer des e-mails qui semblent authentiques.
*   **Contournement des protections :** L'utilisation d'une adresse Google légitime permet de contourner les contrôles DMARC et SPF.
*   **Techniques d'ingénierie sociale :** Les e-mails imitent des notifications d'entreprise courantes pour inciter les victimes à agir.
*   **Chaîne d'attaque à plusieurs étapes :** L'utilisation de plusieurs redirections et d'une fausse page de connexion vise à masquer l'intention malveillante.

**Vulnérabilités :**

Bien qu'aucun numéro CVE spécifique ne soit mentionné dans l'article, la vulnérabilité réside dans la manière dont la fonctionnalité "Send Email" d'Application Integration peut être mal utilisée. L'article ne décrit pas de faille logicielle spécifique dans les services Google Cloud eux-mêmes, mais plutôt une exploitation des capacités d'automatisation existantes.

**Recommandations :**

*   **Prudence accrue face aux notifications automatisées :** Les utilisateurs doivent être vigilants face aux e-mails semblant provenir de services cloud, même s'ils semblent légitimes.
*   **Vérification des liens :** Il est conseillé de survoler les liens avant de cliquer pour vérifier la destination réelle.
*   **Authentification multifacteur (MFA) :** La mise en place de l'authentification multifacteur sur les comptes, en particulier ceux liés à Microsoft, peut atténuer l'impact d'un vol d'identifiants.
*   **Surveillance et blocage par Google :** Google a déjà pris des mesures pour bloquer ces tentatives et travaille à prévenir de futures utilisations abusives de ses services.

---
[Source](https://thehackernews.com/2026/01/cybercriminals-abuse-google-cloud-email.html){:target="_blank"}
