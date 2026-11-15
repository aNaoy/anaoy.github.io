---
title: 'Cursor Says Stolen Fireworks AI Key Led to Trojanized Claude Code Extension Incident'
date: 2026-11-15
permalink: /posts/2026/11/15/cursor-says-stolen-fireworks-ai-key-led-to-trojanized-claude-code-extension-incident/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne d'approvisionnement Cursor via Fireworks AI

Une faille de sécurité chez le fournisseur Fireworks AI a permis à des attaquants d'exfiltrer une clé d'accès appartenant à Cursor, compromettant ainsi plusieurs systèmes et la distribution d'extensions sur sa place de marché.

**Points clés :**
*   **Origine de la fuite :** Une clé d'accès Cursor, exposée par Fireworks AI, a permis aux attaquants d'accéder à un compartiment de stockage contenant des traces de sessions de codage (hors "Privacy Mode").
*   **Données compromises :** Des informations sensibles ont été dérobées, incluant des dépôts de code archivés non-production, des données de support client, des métadonnées d'utilisation et certaines identifiants d'utilisateurs.
*   **Incident de la chaîne d'approvisionnement :** Le 29 octobre 2026, les attaquants ont utilisé des identifiants dérobés pour injecter une version piégée (trojanisée) de l'extension *Claude Code* sur le cache du marketplace de Cursor.
*   **Impact :** Environ 5 000 utilisateurs ont potentiellement téléchargé l'extension malveillante, laquelle tentait d'installer une porte dérobée SSH persistante.
*   **Victimes collatérales :** La brèche chez Fireworks AI a également affecté d'autres entreprises, notamment Uber (données de permis de conduire) et Notion.

**Vulnérabilités :**
*   **Fuite de secrets (Secret Leakage) :** Stockage d'identifiants API dans des logs de session non sécurisés et utilisation d'une clé d'accès tiers insuffisamment protégée par le partenaire (Fireworks AI).
*   **Attaque de la chaîne d'approvisionnement (Supply Chain Attack) :** Manipulation des caches de distribution des extensions pour diffuser du code malveillant aux utilisateurs finaux.
*   *Note : Aucune CVE spécifique n'a été attribuée, l'incident résultant de compromissions d'accès et d'erreurs de configuration.*

**Recommandations :**
*   **Rotation immédiate :** Révocation et rotation systématique de toutes les clés d'accès et identifiants API partagés avec des tiers.
*   **Renforcement de la confidentialité :** Activation systématique du "Privacy Mode" pour empêcher l'entraînement de modèles sur des données contenant potentiellement des secrets ou des informations sensibles.
*   **Gestion des accès :** Mise en place d'un contrôle strict des privilèges sur les dépôts de stockage partagés avec des partenaires externes.
*   **Audit et nettoyage :** Pour les utilisateurs ayant téléchargé les versions 2.1.312 ou 2.1.313 de l'extension *Claude Code*, une réinitialisation des accès et une analyse du système pour détecter toute persistance (type accès SSH non autorisé) sont indispensables.

---
[Source](https://thehackernews.com/2026/11/stolen-fireworks-ai-key-led-to-cursor.html){:target="_blank"}
