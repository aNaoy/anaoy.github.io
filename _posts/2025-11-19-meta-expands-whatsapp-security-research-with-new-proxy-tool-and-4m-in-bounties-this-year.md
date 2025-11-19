---
title: 'Meta Expands WhatsApp Security Research with New Proxy Tool and $4M in Bounties This Year'
date: 2025-11-19
permalink: /posts/2025/11/19/meta-expands-whatsapp-security-research-with-new-proxy-tool-and-4m-in-bounties-this-year/
tags:
- veille-cyber
- hackernews
---
**Renforcement de la Sécurité WhatsApp et Programmes de Récompenses**

Meta a annoncé des initiatives visant à améliorer la sécurité de WhatsApp, notamment la mise à disposition d'un nouvel outil, le "WhatsApp Research Proxy", pour les chercheurs de bugs ayant une longue expérience. Cet outil a pour but de faciliter l'étude du protocole réseau de la messagerie. Parallèlement, une initiative pilote est lancée pour encourager les équipes de recherche académique à se concentrer sur les abus de la plateforme, avec un soutien accru de la part de Meta.

Au cours des 15 dernières années, Meta a attribué plus de 25 millions de dollars en récompenses de bugs à plus de 1 400 chercheurs. Rien que cette année, plus de 4 millions de dollars ont été distribués pour près de 800 rapports valides, sur un total d'environ 13 000 soumissions reçues.

**Points Clés et Vulnérabilités :**

*   **Outil de Recherche WhatsApp:** Un nouveau proxy est mis à la disposition de chercheurs de confiance pour faciliter l'analyse du protocole réseau de WhatsApp.
*   **Programme de Récompenses de Bugs:** Augmentation des récompenses, avec plus de 4 millions de dollars versés cette année pour environ 800 rapports valides. Lancement d'initiatives pour attirer davantage de chercheurs académiques.
*   **Vulnérabilité d'Enregistrement de Contenu (Non CVE spécifié):** Une faille antérieure à v2.25.23.73 sur Android, v2.25.23.82 sur iOS et v2.25.23.83 sur Mac aurait pu permettre à un utilisateur de déclencher le traitement de contenu à partir d'une URL arbitraire sur l'appareil d'un autre utilisateur. Aucune exploitation active n'a été constatée.
*   **CVE-2025-59489 (CVSS 8.4):** Une vulnérabilité au niveau du système d'exploitation des appareils Quest, découverte par RyotaK de Flatt Security, qui permettait à des applications malveillantes de manipuler des applications Unity pour exécuter du code arbitraire. Un correctif au niveau du système d'exploitation a été déployé par Meta.
*   **Protection Anti-Scraping:** Des protections ont été ajoutées à WhatsApp suite à une étude qui détaillait une méthode d'énumération à grande échelle des comptes WhatsApp et la constitution d'une base de données d'informations publiques, de photos de profil et de textes "À propos", en contournant les limitations de débit du service. Bien que cette méthode ait permis de découvrir des comptes dans des pays où WhatsApp est officiellement interdit (comme la Chine et le Myanmar), Meta n'a constaté aucune preuve d'abus malveillant de cette faille, et les messages des utilisateurs sont restés chiffrés de bout en bout.
*   **Risques liés aux Accusés de Réception (Pas de CVE spécifié):** Une recherche antérieure a mis en évidence comment les accusés de réception pouvaient poser des risques pour la vie privée, permettant à un attaquant d'obtenir des informations sur l'activité d'un utilisateur, de suivre son activité sur différents appareils, ou de connaître son emploi du temps, sans aucune notification pour la cible.

**Recommandations :**

Les mesures mises en place par Meta, incluant le nouvel outil de recherche, les programmes de récompenses de bugs et l'ajout de protections anti-scraping, visent à renforcer la sécurité de la plateforme WhatsApp et à encourager la découverte et la correction proactive des vulnérabilités. Les utilisateurs bénéficient de la protection du chiffrement de bout en bout pour leurs messages.

---
[Source](https://thehackernews.com/2025/11/meta-expands-whatsapp-security-research.html){:target="_blank"}
