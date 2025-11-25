---
title: 'Stop Putting Your Passwords Into Random Websites (Yes, Seriously, You Are The Problem)'
date: 2025-11-25
permalink: /posts/2025/11/25/stop-putting-your-passwords-into-random-websites-yes-seriously-you-are-the-problem/
tags:
- veille-cyber
- zerodaysfans
---
### Exposer accidentellement de secrets : un problème d'utilisateurs, pas d'outils

Des recherches récentes ont révélé une quantité alarmante de données sensibles, notamment des identifiants, des clés et des informations d'authentification, exposées publiquement via des outils en ligne populaires de formatage de code tels que JSONFormatter et CodeBeautify. Ces plateformes, conçues pour améliorer la lisibilité du code, offrent une fonctionnalité "Sauvegarder" qui génère des liens partageables, souvent mal interprétés par les utilisateurs. Le résultat est une prolifération de secrets d'entreprise, allant des identifiants Active Directory aux clés API et aux informations KYC, émanant d'organisations critiques dans des secteurs tels que la finance, le gouvernement, la cybersécurité et la santé.

**Points Clés :**

*   Des outils de formatage de code populaires comme JSONFormatter et CodeBeautify ont été utilisés par inadvertance pour exposer des données sensibles.
*   La fonctionnalité de sauvegarde et de partage de ces outils a conduit à la divulgation de plus de 80 000 soumissions contenant des secrets.
*   Les secrets exposés incluent une vaste gamme d'informations critiques, affectant de nombreux secteurs d'activité.
*   Des efforts de sensibilisation ont été faits auprès des organisations concernées, mais la réponse a été mitigée.
*   D'autres acteurs malveillants scannent déjà ces plateformes à la recherche de données exposées.

**Vulnérabilités :**

Bien qu'aucun CVE spécifique ne soit mentionné dans l'article, la vulnérabilité découle de la mauvaise utilisation des fonctionnalités de ces outils en ligne. La principale faille réside dans la **gestion des identifiants et secrets par les utilisateurs** lorsqu'ils manipulent des données sensibles dans des environnements non sécurisés. Les liens "sauvegardés" et partageables créent une surface d'attaque accessible publiquement.

**Recommandations :**

*   **Éviter de saisir des informations sensibles** (identifiants, clés API, mots de passe, etc.) dans des outils en ligne publics ou non approuvés pour le formatage ou la manipulation de code.
*   **Utiliser des environnements de développement et de test sécurisés et internes** pour la manipulation de données sensibles.
*   **Mettre en place des politiques strictes** concernant la gestion des secrets et des données confidentielles au sein des organisations.
*   **Sensibiliser régulièrement les employés** aux risques liés au partage d'informations sensibles en ligne.
*   **Privilégier les outils locaux ou les solutions d'entreprise sécurisées** pour les tâches de formatage et de développement.
*   **Implémenter des processus de revue de code et de configuration** pour détecter les secrets potentiellement exposés avant leur mise en production.

---
[Source](https://labs.watchtowr.com/stop-putting-your-passwords-into-random-websites-yes-seriously-you-are-the-problem/){:target="_blank"}
