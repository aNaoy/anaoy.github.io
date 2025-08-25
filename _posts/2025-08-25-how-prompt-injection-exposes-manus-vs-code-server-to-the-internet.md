---
title: 'How Prompt Injection Exposes Manus VS Code Server to the Internet'
date: 2025-08-25
permalink: /posts/2025/08/25/how-prompt-injection-exposes-manus-vs-code-server-to-the-internet/
tags:
- veille-cyber
- zerodaysfans
---
**Exposition de Manus via Injection de Prompt : De la faille à la prise de contrôle**

Une faille de sécurité critique a été découverte dans l'agent IA Manus, permettant à des acteurs malveillants de prendre le contrôle de son environnement de développement (dev box). L'attaque exploite une vulnérabilité d'injection de prompt indirecte pour exposer le serveur VS Code interne de Manus sur Internet, puis exfiltrer les informations d'identification nécessaires pour un accès non autorisé.

**Points Clés :**

*   **Injection de Prompt :** Manus est sensible aux instructions malveillantes insérées dans des données non fiables, ce qui déclenche des actions imprévues.
*   **Exposition de Port sans Contrôle :** L'outil `deploy_expose_port` de Manus peut exposer des ports locaux sur Internet sans vérification humaine ou mesures de sécurité (comme des restrictions d'IP). La réponse de cet outil inclut l'URL publique du port exposé.
*   **Serveur VS Code :** Manus utilise un serveur VS Code dont le mot de passe est stocké localement sur la machine.
*   **Fuite de Données :** Deux canaux permettent à Manus de divulguer des informations vers des serveurs tiers :
    *   Un outil de navigation (`browsing tool`) pouvant accéder à des domaines non fiables sans supervision.
    *   Le rendu d'images via la syntaxe Markdown provenant de sources non fiables, permettant d'encoder des données dans les URLs des images.

L'enchaînement de ces vulnérabilités ("le trifecta létal") permet à un attaquant d'obtenir l'URL publique et le mot de passe du serveur VS Code, menant à une prise de contrôle totale de la machine hôte.

**Vulnérabilités Identifiées :**

*   **Injection de Prompt Indirecte :** Permet l'exécution d'actions non désirées en manipulant les entrées de l'IA.
*   **Exposition de Port Non Sécurisée :** L'outil `deploy_expose_port` manque de contrôles d'accès et de validation, permettant l'exposition de services internes.
*   **Canaux d'Exfiltration de Données :**
    *   Utilisation de l'outil de navigation vers des domaines non approuvés.
    *   Rendu d'images via Markdown à partir de sources externes, permettant l'encodage de données sensibles dans les URLs d'images.

Aucun identifiant CVE spécifique n'est mentionné dans l'article pour ces vulnérabilités.

**Recommandations et Atténuations :**

*   **Contrôle d'Accès Réseau :** Permettre la gestion des domaines et serveurs auxquels Manus peut se connecter. Restreindre l'accès aux ports exposés à des adresses IP pré-approuvées (liste blanche).
*   **Validation Humaine :** Exiger une confirmation humaine avant d'exécuter des actions potentiellement dangereuses, comme l'exposition de ports ou l'utilisation d'outils sensibles.
*   **Blocage du Rendu d'Images :** Mettre en place des politiques de sécurité (ex: Content-Security-Policy) pour bloquer le rendu d'images provenant de domaines non fiables.
*   **Détection d'Injection de Prompt :** Améliorer les mécanismes de détection pour identifier et atténuer les attaques par injection de prompt, potentiellement via un "moniteur d'injection de prompt".
*   **Transparence et Documentation :** Mettre à jour la documentation et l'interface utilisateur pour informer les utilisateurs des limitations de sécurité de Manus et des risques potentiels.

---
[Source](https://embracethered.com/blog/posts/2025/manus-ai-kill-chain-expose-port-vs-code-server-on-internet/){:target="_blank"}
