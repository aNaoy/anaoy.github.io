---
title: 'Google Chrome Adds ClickFix Warnings to Stop Users From Running Malicious Commands'
date: 2026-10-21
permalink: /posts/2026/10/21/google-chrome-adds-clickfix-warnings-to-stop-users-from-running-malicious-commands/
tags:
- veille-cyber
- hackernews
---
### Renforcement de la sécurité contre les attaques ClickFix et le tracking web

Google Chrome déploie de nouvelles mesures de protection pour contrer la technique d'ingénierie sociale dite « ClickFix ». Cette méthode incite les utilisateurs à copier-coller des commandes malveillantes (souvent déguisées en processus de dépannage ou de vérification type reCAPTCHA) directement dans leur terminal ou boîte de dialogue Windows/Mac, contournant ainsi les protections de sécurité classiques du navigateur.

**Points clés :**
*   **Mécanisme de l'attaque :** Les attaquants utilisent des techniques "Living-off-the-Land" (LotL) comme PowerShell pour exécuter des charges utiles sans passer par un téléchargement de fichier classique détectable par le navigateur.
*   **Protection Chrome :** Si la fonction « Navigation sécurisée renforcée » est active, Chrome analyse désormais le contenu du presse-papier. Si une commande suspecte est détectée avant l'exécution, une alerte est affichée à l'utilisateur.
*   **Défenses supplémentaires :** Google intègre des modèles de langage (LLM) sur l'appareil pour identifier les arnaques au support technique et durcit la vérification des services financiers pour les annonceurs.
*   **Safari/WebKit :** En complément, Apple a introduit une protection contre le "Identity Resolution", une technique permettant de créer des identifiants de suivi persistants à partir des adresses e-mail saisies sur des sites web.

**Vulnérabilités :**
*   Pas de CVE spécifique associée : il s'agit d'une technique d'exploitation de **l'ingénierie sociale** et du détournement d'outils système légitimes (PowerShell, cmd.exe) plutôt que d'une faille logicielle directe.

**Recommandations :**
*   **Activer la protection renforcée :** Dans les paramètres de sécurité de Google Chrome, assurez-vous que l'option « Navigation sécurisée renforcée » (Enhanced Protection) est activée.
*   **Prudence avec les commandes :** Ne jamais copier-coller de commandes fournies par des sites web dans un terminal (PowerShell, CMD, Terminal Mac), surtout si celles-ci sont présentées comme une solution à une erreur technique soudaine.
*   **Vigilance :** Se méfier des fenêtres surgissantes invitant à une vérification "humaine" par le biais de commandes système, une pratique devenue un vecteur d'infection majeur pour les chevaux de Troie d'accès à distance (RAT).

---
[Source](https://thehackernews.com/2026/10/google-chrome-adds-clickfix-warnings-to.html){:target="_blank"}
