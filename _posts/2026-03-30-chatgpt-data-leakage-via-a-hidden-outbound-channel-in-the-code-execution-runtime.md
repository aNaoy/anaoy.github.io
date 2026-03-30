---
title: 'ChatGPT Data Leakage via a Hidden Outbound Channel in the Code Execution Runtime'
date: 2026-03-30
permalink: /posts/2026/03/30/chatgpt-data-leakage-via-a-hidden-outbound-channel-in-the-code-execution-runtime/
tags:
- veille-cyber
- zerodaysfans
---
### Exfiltration de données via un canal DNS dissimulé dans ChatGPT

Des chercheurs de Check Point ont découvert une vulnérabilité critique au sein de l'environnement d'exécution de code (Python) de ChatGPT, permettant de contourner les restrictions de sécurité pour exfiltrer des données ou établir un accès distant (shell).

**Points clés :**
*   **Canal caché :** L'attaque exploite une faille dans la gestion du trafic réseau au sein de l'environnement isolé (bac à sable). Bien que l'accès direct à Internet soit bloqué, les requêtes DNS restent autorisées.
*   **DNS Tunneling :** Les données sensibles (messages, documents téléchargés, analyses) sont encodées dans des requêtes DNS, créant un tunnel discret vers un serveur contrôlé par l'attaquant.
*   **Invisibilité :** Le processus fonctionne sans déclencher les alertes habituelles de l'interface, contournant les mécanismes de consentement utilisateur pour les partages de données externes.
*   **Vecteurs d'attaque :** La vulnérabilité peut être déclenchée par un simple prompt malveillant (social engineering) ou via des GPT personnalisés (GPTs) embarquant des instructions malveillantes.
*   **Accès distant :** Le tunnel permet non seulement l'exfiltration, mais aussi l'exécution de commandes distantes (Remote Shell) dans l'environnement Linux sous-jacent.

**Vulnérabilités :**
*   **Nature :** Exploitation du protocole DNS pour établir un canal de communication bidirectionnel (Data Exfiltration & Command Execution) depuis un environnement isolé.
*   **CVE :** Aucune CVE n'est mentionnée pour cet incident spécifique, OpenAI ayant identifié et corrigé la faille en interne.

**Recommandations :**
*   **Statut :** La vulnérabilité a été signalée par Check Point et corrigée par OpenAI (déploiement finalisé le 20 février 2026).
*   **Bonnes pratiques :** Bien que le problème soit résolu, il est conseillé de rester vigilant lors de l'utilisation de GPTs tiers. Évitez de copier des prompts issus de sources non fiables promettant des "fonctionnalités cachées" ou un accès "premium" gratuit, car ceux-ci peuvent être utilisés pour injecter des commandes malveillantes dans votre session de travail.
*   **Gestion des données :** Soyez prudent lors du téléchargement de documents hautement confidentiels (médicaux, financiers ou juridiques) dans des environnements d'IA, même si ceux-ci semblent isolés.

---
[Source](https://research.checkpoint.com/2026/chatgpt-data-leakage-via-a-hidden-outbound-channel-in-the-code-execution-runtime/){:target="_blank"}
