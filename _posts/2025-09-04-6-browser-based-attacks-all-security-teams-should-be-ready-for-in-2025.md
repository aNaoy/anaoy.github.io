---
title: '6 browser-based attacks all security teams should be ready for in 2025'
date: 2025-09-04
permalink: /posts/2025/09/04/6-browser-based-attacks-all-security-teams-should-be-ready-for-in-2025/
tags:
- veille-cyber
- bleepingcomp
---
**Le Navigateur : Un Champ de Bataille pour la Cybersécurité en 2025**

L'environnement de travail moderne a déplacé le champ de bataille de la cybersécurité vers le navigateur web, devenant le principal vecteur d'attaques contre les applications et les données d'entreprise. Les équipes de sécurité doivent se préparer à six techniques d'attaque courantes exploitant le navigateur pour accéder aux services tiers, qui sont devenus la cible privilégiée des cybercriminels, menant à des violations de données massives et à des rançonnements.

**Points Clés :**

*   **Le navigateur comme nouvelle frontière :** Les attaquants ciblent les utilisateurs à travers le navigateur pour compromettre les applications et les données d'entreprise.
*   **Évolution des attaques :** Les méthodes traditionnelles comme le phishing ont évolué pour contourner les défenses actuelles.
*   **Visibilité navigateur essentielle :** La détection et la réponse efficaces nécessitent une visibilité au niveau du navigateur pour analyser les interactions en temps réel.

**Vulnérabilités et Techniques d'Attaque :**

1.  **Phishing pour identifiants et sessions :**
    *   **Description :** Utilisation de kits "Attacker-in-the-Middle" (AitM) pour intercepter les sessions des utilisateurs, contournant ainsi la plupart des formes d'authentification multifacteur (MFA).
    *   **Mécanisme :** Diffusion via divers canaux (messagerie instantanée, réseaux sociaux, SMS, publicités malveillantes), utilisation de code JavaScript obfusqué, protection anti-bot, et hébergement sur des services légitimes pour échapper aux détections traditionnelles.
    *   **CVEs :** Non spécifié dans l'article, mais les techniques AitM sont largement documentées dans la communauté de la sécurité.

2.  **Distribution de code malveillant (ClickFix, FileFix) :**
    *   **Description :** Tromper les utilisateurs pour qu'ils exécutent des commandes malveillantes sur leur appareil via des défis de vérification dans le navigateur (ex: faux CAPTCHA). Les variantes comme FileFix utilisent la barre d'adresse de l'explorateur de fichiers pour exécuter des commandes.
    *   **Objectif :** Livrer des logiciels espions (infostealers) pour voler des cookies de session et des identifiants.
    *   **CVEs :** Non spécifié.

3.  **Intégrations OAuth malveillantes :**
    *   **Description :** Inciter les utilisateurs à autoriser des applications tierces contrôlées par l'attaquant, leur accordant ainsi un accès aux données et aux fonctionnalités des applications légitimes.
    *   **Mécanisme :** Contourne les processus de connexion et d'authentification traditionnels, y compris les MFA résistantes, comme démontré par les récentes attaques sur Salesforce via le flux d'autorisation de code d'appareil.
    *   **CVEs :** Non spécifié.

4.  **Extensions de navigateur malveillantes :**
    *   **Description :** Installation d'extensions frauduleuses ou prise de contrôle d'extensions existantes pour capturer des identifiants, voler des cookies de session, ou injecter du contenu malveillant.
    *   **Mécanisme :** Facilité par l'achat d'extensions et les mises à jour malveillantes. Les autorisations larges accordées aux extensions sont particulièrement dangereuses.
    *   **CVEs :** Non spécifié, mais les risques associés aux permissions d'extensions sont bien connus.

5.  **Distribution de fichiers malveillants :**
    *   **Description :** Distribution de fichiers (ex: HTA, SVG) contenant des liens vers du contenu malveillant ou des pages de phishing client-side pour voler des identifiants.
    *   **Mécanisme :** Exploitation de divers canaux de distribution, y compris les malvertising et les attaques drive-by.
    *   **CVEs :** Non spécifié.

6.  **Identifiants volés et lacunes MFA :**
    *   **Description :** Utilisation d'identifiants compromis (via phishing ou logiciels espions) pour accéder à des comptes non protégés par la MFA ou pour exploiter des "connexions fantômes" locales qui ne nécessitent pas de MFA.
    *   **Impact :** Permet de prendre le contrôle d'applications critiques, comme vu dans les incidents Snowflake et Jira.
    *   **CVEs :** Non spécifié.

**Recommandations :**

*   **Mettre en place une visibilité au niveau du navigateur :** Les solutions de sécurité basées sur le navigateur peuvent détecter et analyser les interactions des utilisateurs en temps réel, offrant une visibilité sur les extensions, les intégrations OAuth, et les téléchargements de fichiers.
*   **Gérer activement les extensions de navigateur :** Les équipes de sécurité doivent surveiller et contrôler les extensions installées par les employés, identifier les extensions à risque, et comparer avec des listes de malveillances connues.
*   **Renforcer la gestion des identités et des accès :** Examiner et durcir la configuration de la sécurité des applications, notamment en assurant une couverture MFA complète et en identifiant et corrigeant les "connexions fantômes" ou les lacunes dans la couverture SSO.
*   **Contrôler les intégrations d'applications tierces :** Gérer rigoureusement les autorisations accordées aux applications tierces via OAuth et surveiller les intégrations potentiellement malveillantes.
*   **Observer les actions dans le navigateur :** Identifier des comportements suspects tels que la copie de code depuis le presse-papiers de la page, qui est un indicateur clé d'attaques comme ClickFix.

---
[Source](https://www.bleepingcomputer.com/news/security/6-browser-based-attacks-all-security-teams-should-be-ready-for-in-2025/){:target="_blank"}
