---
title: 'Attackers AI Agents Found a Zero-Day in Medical-Imaging Software and Gained Root Access'
date: 2026-11-21
permalink: /posts/2026/11/21/attackers-ai-agents-found-a-zero-day-in-medical-imaging-software-and-gained-root-access/
tags:
- veille-cyber
- hackernews
---
### Utilisation d'agents IA autonomes pour l'exploitation d'une faille critique dans MONAI Label

Des attaquants liés à la Chine ont utilisé des agents IA autonomes, via le framework de test d'intrusion « Cairn », pour identifier et exploiter une vulnérabilité « zero-day » dans le logiciel d'imagerie médicale MONAI Label. Les agents ont réussi, en seulement 11 minutes, à exploiter cette faille pour obtenir un accès à distance, puis, lors d'une phase ultérieure, à élever leurs privilèges jusqu'à obtenir un accès root sur un serveur universitaire.

**Points clés :**
*   **Automatisation offensive :** Les agents IA ont fonctionné de manière autonome, définissant eux-mêmes les méthodes d'attaque après avoir reçu un objectif global de la part des opérateurs.
*   **Vecteur d'attaque :** La vulnérabilité est une faille de type *path traversal* (traversée de répertoire) permettant l'écriture arbitraire de fichiers hors du dossier de stockage prévu.
*   **Gravité :** Le score CVSS est de 9.8 (critique).
*   **Disponibilité du correctif :** Bien qu'un correctif ait été fusionné dans le code source, aucune version officielle corrigée n'est encore disponible au téléchargement.

**Vulnérabilité :**
*   **CVE-2026-133968 :** Faille de *path traversal* affectant MONAI Label 0.8.5 et les versions antérieures, permettant à un attaquant non authentifié d'écrire des fichiers sur le serveur.

**Recommandations :**
*   **Isolation réseau :** Bloquer l'accès non autorisé aux serveurs via des règles de pare-feu strictes (ne pas se contenter d'obscurcir les URL).
*   **Durcissement de la configuration :** Activer impérativement l'authentification (désactivée par défaut).
*   **Principe du moindre privilège :** Exécuter le service sous un compte utilisateur limité (jamais en root) et restreindre strictement les droits d'écriture sur le système de fichiers.
*   **Audit post-compromission :** Rechercher tout fichier de démarrage Python suspect ou toute tâche d'entraînement anormale sur les systèmes exposés.
*   **Veille :** Surveiller la publication d'une version stable intégrant officiellement le correctif du 19 octobre.

---
[Source](https://thehackernews.com/2026/11/attackers-ai-agents-found-zero-day-in.html){:target="_blank"}
