---
title: '6 Browser-Based Attacks Security Teams Need to Prepare For Right Now'
date: 2025-09-15
permalink: /posts/2025/09/15/6-browser-based-attacks-security-teams-need-to-prepare-for-right-now/
tags:
- veille-cyber
- hackernews
---
### Les menaces modernes qui exploitent le navigateur

Les attaques ciblant les utilisateurs via leur navigateur web ont considérablement augmenté, visant à compromettre les applications professionnelles et les données sensibles. Le passage à des applications internet décentralisées et des canaux de communication variés rend les utilisateurs plus vulnérables.

**Points clés :**

*   Les attaques évoluent pour contourner les défenses traditionnelles basées sur les e-mails et le réseau.
*   Le navigateur est devenu un point d'accès privilégié pour les attaquants.

**Vulnérabilités et menaces identifiées :**

1.  **Phishing de credentials et de sessions :** Utilisation de divers canaux (messageries instantanées, réseaux sociaux, SMS, publicités malveillantes) pour voler identifiants et cookies de session. Les kits de phishing modernes contournent les MFA grâce à des techniques d'obfuscation, de protection anti-bot et d'hébergement sur des services légitimes.
2.  **Copier-coller malveillant (ClickFix, FileFix) :** Trompe les utilisateurs pour exécuter des commandes malveillantes via des fausses vérifications (CAPTCHA, etc.) ou l'explorateur de fichiers. L'objectif est souvent de déployer des logiciels espions (infostealers).
3.  **Intégrations OAuth malveillantes (consent phishing) :** Incite les utilisateurs à autoriser des applications tierces contrôlées par l'attaquant, contournant ainsi les mécanismes d'authentification traditionnels, y compris le MFA résistant au phishing (comme les passkeys). Les attaques sur Salesforce via le flux d'autorisation de code d'appareil sont un exemple récent.
4.  **Extensions de navigateur malveillantes :** Permettent de capturer les connexions ou d'extraire des cookies et identifiants sauvegardés. Les attaquants peuvent créer leurs propres extensions ou compromettre des extensions existantes pour contourner les contrôles de sécurité des magasins d'applications.
5.  **Distribution de fichiers malveillants :** Envoi de fichiers (exécutables, HTA, SVG) via des canaux variés. Ces fichiers peuvent déployer des malwares, contenir des liens vers des pages malveillantes, ou agir comme des pages de phishing client-side.
6.  **Identifiants volés et lacunes MFA :** Les identifiants compromis via phishing ou infostealers sont utilisés pour accéder à des comptes sans authentification multifacteur (MFA) activée ou correctement configurée. Des vulnérabilités comme les "ghost logins" (connexions locales qui acceptent des mots de passe sans MFA) subsistent même avec le Single Sign-On (SSO).

**Recommandations :**

*   Les équipes de sécurité doivent se concentrer sur la visibilité et la réponse aux menaces au niveau du navigateur.
*   Les employés ne devraient pas installer d'extensions de navigateur sans approbation préalable de l'équipe de sécurité.
*   Il est crucial de surveiller et de corriger les configurations de sécurité des applications, notamment la couverture MFA et les intégrations OAuth.
*   Enregistrer les téléchargements de fichiers dans le navigateur peut renforcer la protection contre les attaques côté client ou les redirections vers du contenu malveillant.
*   Une surveillance des identifiants et des méthodes de connexion peut aider à identifier et corriger les failles de sécurité avant qu'elles ne soient exploitées.

---
[Source](https://thehackernews.com/2025/09/6-browser-based-attacks-security-teams.html){:target="_blank"}
