---
title: 'OpenAI is preparing “o,” an always-on ChatGPT assistant that could handle email'
date: 2026-09-28
permalink: /posts/2026/09/28/openai-is-preparing-o-an-always-on-chatgpt-assistant-that-could-handle-email/
tags:
- veille-cyber
- bleepingcomp
---
### L'assistant "o" : OpenAI prépare une IA persistante et connectée

OpenAI développe actuellement "o", un nouvel assistant intelligent conçu pour fonctionner en arrière-plan ("always-on"). Cette fonctionnalité, repérée au sein de l'offre ChatGPT Pro, semble destinée à automatiser des tâches complexes, notamment la gestion des courriels grâce à une configuration technique dédiée (`email_suffix`).

**Points clés :**
*   **Persistance :** Contrairement au modèle actuel, l'assistant "o" est conçu pour rester actif et assister l'utilisateur même hors des sessions de chat directes.
*   **Intégration e-mail :** La présence de suffixes e-mail dans les fichiers de configuration suggère une future capacité d'interaction autonome avec la messagerie de l'utilisateur.
*   **Annonce attendue :** OpenAI devrait dévoiler plus de détails techniques sur cet outil lors de sa conférence *DevDay 2026*, prévue le 29 septembre.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée à cette fonctionnalité pour le moment, le produit étant encore au stade de développement/test.
*   **Risques potentiels :** L'activation d'un assistant "toujours actif" ayant accès aux e-mails et au contenu privé augmente drastiquement la surface d'attaque, notamment face aux risques d'exfiltration de données, d'hameçonnage automatisé (via l'IA) ou d'usurpation d'identité en cas de compromission du compte utilisateur.

**Recommandations :**
*   **Surveillance des accès :** Si cette fonctionnalité est déployée, appliquez le principe du moindre privilège en limitant strictement les accès de l'assistant aux seules boîtes mail nécessaires.
*   **Authentification :** Renforcez la sécurisation des comptes OpenAI associés à ces outils par une authentification multifacteur (MFA) robuste.
*   **Veille :** Surveillez les annonces officielles du *DevDay 2026* pour évaluer les mesures de confidentialité et les paramètres de contrôle utilisateur mis en place avant d'autoriser l'accès à des données sensibles.

---
[Source](https://www.bleepingcomputer.com/news/artificial-intelligence/openai-is-preparing-o-an-always-on-chatgpt-assistant-that-could-handle-email/){:target="_blank"}
