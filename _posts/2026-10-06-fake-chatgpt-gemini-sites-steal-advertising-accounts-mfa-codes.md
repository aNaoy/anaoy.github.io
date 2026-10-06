---
title: 'Fake ChatGPT, Gemini Sites steal advertising accounts, MFA codes'
date: 2026-10-06
permalink: /posts/2026/10/06/fake-chatgpt-gemini-sites-steal-advertising-accounts-mfa-codes/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne de phishing sophistiquée via des faux outils IA

Une vaste campagne de cyberattaques cible les gestionnaires de comptes publicitaires en usurpant l'identité de plateformes d'IA populaires (ChatGPT, Gemini, Claude, Perplexity). Les attaquants exploitent le lancement de nouveaux outils, comme « Muse AI » de Meta, pour inciter les professionnels à connecter leurs comptes à de faux services.

**Points clés :**
*   **Cible :** Agences média, acheteurs publicitaires et administrateurs gérant des budgets importants.
*   **Objectif :** Voler les identifiants et les codes d'authentification multifacteur (MFA) pour détourner des budgets publicitaires ou revendre les comptes compromis.
*   **Technique utilisée :** L'attaque *Browser-in-the-Browser* (BitB), qui consiste à générer une fenêtre de connexion frauduleuse à l'intérieur d'une page web pour imiter une fenêtre système légitime.
*   **Interaction humaine :** Un opérateur humain pilote l'attaque en temps réel, permettant de contourner dynamiquement les protections MFA (codes SMS, jetons d'authentification, notifications push Okta ou QR codes).
*   **Infrastructure :** La campagne est orchestrée via un kit de phishing complexe utilisant Next.js et Socket.IO, avec des serveurs back-end sur Railway ou Render.

**Vulnérabilités exploitées :**
*   Il ne s'agit pas d'une vulnérabilité logicielle spécifique (CVE), mais de l'exploitation de la technique **BitB** qui tire parti de la confiance des utilisateurs dans les interfaces de fenêtres contextuelles (pop-ups).
*   L'utilisation de dépôts GitHub mal configurés par les attaquants a permis de confirmer la persistance de cette opération depuis mars.

**Recommandations :**
*   **Vérifier la fenêtre :** Les fenêtres BitB étant des `iframes`, elles ne peuvent pas être déplacées hors de la zone de la fenêtre du navigateur ni redimensionnées. Tentez de glisser la fenêtre en dehors des limites du navigateur pour tester sa légitimité.
*   **Méfiance accrue :** Soyez vigilant face aux invitations "Connecter mon compte" provenant de sites tiers, même s'ils imitent l'interface de fournisseurs connus (Google, Meta, etc.).
*   **Analyse de l'URL :** Vérifiez systématiquement le nom de domaine réel dans la barre d'adresse avant de saisir des informations sensibles.
*   **Authentification :** Privilégiez les clés de sécurité physiques (FIDO2/WebAuthn) qui sont plus résistantes au phishing que les codes SMS ou les notifications push standard, car elles lient l'authentification à l'origine réelle du domaine.

---
[Source](https://www.bleepingcomputer.com/news/security/fake-chatgpt-gemini-sites-steal-advertising-accounts-mfa-codes/){:target="_blank"}
