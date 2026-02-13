---
title: 'Malicious Chrome Extensions Caught Stealing Business Data, Emails, and Browsing History'
date: 2026-02-13
permalink: /posts/2026/02/13/malicious-chrome-extensions-caught-stealing-business-data-emails-and-browsing-history/
tags:
- veille-cyber
- hackernews
---
## Extensions Malveillantes sur Chrome : Exploitation de Données d'Entreprise et Historique de Navigation

Des extensions malveillantes pour le navigateur Google Chrome ont été découvertes, conçues pour voler des données sensibles, des emails et l'historique de navigation. Ces extensions, se faisant passer pour des outils légitimes, ciblent des plateformes comme Meta Business Suite, Facebook Business Manager, et des assistants basés sur l'IA.

**Points Clés :**

*   **CL Suite :** Une extension qui prétend améliorer l'utilisation de Meta Business Suite, mais qui vole en réalité les codes d'authentification à deux facteurs (2FA), les listes de contacts des gestionnaires d'entreprise, et les données analytiques. Ces informations sont envoyées à une infrastructure contrôlée par l'attaquant.
*   **VK Styles :** Un ensemble d'extensions conçues pour détourner les comptes VKontakte, en s'abonnant automatiquement à des groupes, en modifiant les paramètres du compte et en maintenant un contrôle persistant.
*   **AiFrame :** Un groupe de 32 extensions se présentant comme des assistants IA (résumé, chat, écriture, aide Gmail) qui siphonnnent des données sensibles en utilisant des iframes distants pour accéder aux fonctionnalités du navigateur. Certaines ciblent spécifiquement Gmail pour lire le contenu des emails.
*   **Exfiltration d'Historique de Navigation :** Une large collection de 287 extensions a été identifiée comme exfiltrant l'historique de navigation vers des courtiers de données, avec un total de 37,4 millions d'installations.

**Vulnérabilités et Méthodes d'Attaque :**

*   **Vol de Secrets TOTP et Codes 2FA :** L'extension CL Suite collecte les secrets utilisés pour générer les codes TOTP et les codes 2FA eux-mêmes.
*   **Extraction de Données d'Entreprise :** Ces extensions peuvent extraire des listes de personnes (noms, emails, rôles, permissions) et des informations sur les actifs liés aux gestionnaires d'entreprise (comptes publicitaires, pages, configurations de paiement).
*   **Manipulation de Comptes VKontakte :** Vol de jetons CSRF pour contourner la sécurité, modification des paramètres du compte, et abonnements forcés à des groupes.
*   **Accès à Distance via Iframes :** Les extensions AiFrame utilisent des iframes pour exécuter du code distant et accéder aux données du navigateur, y compris le contenu des emails dans le cas de Gmail.
*   **Exfiltration d'Historique de Navigation :** Collection de l'historique de navigation pour la revente à des courtiers de données.

**Recommandations :**

*   **Minimalisme et Vigilance :** Installer uniquement les extensions nécessaires, provenant de sources fiables et avec de bonnes critiques.
*   **Audit Périodique :** Examiner régulièrement les extensions installées pour détecter tout comportement suspect ou demande d'autorisations excessives.
*   **Profils de Navigation Séparés :** Utiliser des profils de navigateur distincts pour les tâches sensibles afin de limiter l'impact en cas de compromission.
*   **Liste Blanche d'Extensions :** Pour les organisations, implémenter une politique de liste blanche pour autoriser uniquement les extensions approuvées.
*   **Attention aux Autorisations :** Examiner attentivement les autorisations demandées par une extension avant de l'installer.
*   **Mises à Jour Régulières :** S'assurer que le navigateur et les extensions sont maintenus à jour pour bénéficier des derniers correctifs de sécurité.

---
[Source](https://thehackernews.com/2026/02/malicious-chrome-extensions-caught.html){:target="_blank"}
