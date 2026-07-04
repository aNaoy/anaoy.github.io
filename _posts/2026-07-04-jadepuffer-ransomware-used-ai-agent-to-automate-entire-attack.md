---
title: 'JadePuffer ransomware used AI agent to automate entire attack'
date: 2026-07-04
permalink: /posts/2026/07/04/jadepuffer-ransomware-used-ai-agent-to-automate-entire-attack/
tags:
- veille-cyber
- bleepingcomp
---
### JadePuffer : L'émergence des cyberattaques automatisées par IA

Le groupe JadePuffer a marqué une étape décisive en utilisant un agent IA basé sur un grand modèle de langage (LLM) pour mener une opération de ransomware complète et autonome. Ce système est capable d'effectuer des phases de reconnaissance, de vol de données, de mouvement latéral, d'élévation de privilèges et de chiffrement, tout en s'adaptant en temps réel aux obstacles rencontrés durant l'intrusion.

**Points clés :**
*   **Adaptabilité :** L'agent IA analyse les échecs (par exemple, une erreur de parsing) et ajuste ses paramètres de manière autonome en quelques secondes.
*   **Comportement :** L'attaque inclut des commentaires en langage naturel dans le code généré, démontrant une capacité de raisonnement opérationnel propre aux modèles d'IA.
*   **Méthodologie :** Après compromission initiale, l'agent a exfiltré des données, établi une persistance par tâche planifiée (cron job), et pivoté vers des serveurs MySQL pour chiffrer les configurations des services.

**Vulnérabilités exploitées :**
*   **CVE-2025-3248 :** Exécution de code à distance (RCE) non authentifiée dans le framework Langflow.
*   **CVE-2021-29441 :** Contournement d'authentification dans Alibaba Nacos, permettant la création de comptes administrateurs factices.

**Recommandations :**
*   **Durcissement des serveurs :** Sécuriser les endpoints exposés sur Internet, en particulier ceux utilisant des frameworks LLM qui contiennent souvent des clés API ou des identifiants cloud critiques.
*   **Gestion des accès :** Appliquer le principe du moindre privilège, notamment sur les bases de données et les services de configuration (comme Nacos/MinIO) pour limiter l'impact en cas de mouvement latéral.
*   **Surveillance et détection :** Tirer parti des nouvelles opportunités de détection offertes par les payloads générés par IA, qui présentent des structures et des itérations distinctes des attaques manuelles classiques.
*   **Mises à jour :** Appliquer systématiquement les correctifs de sécurité dès leur publication, comme pour la faille Langflow corrigée en avril 2025.

---
[Source](https://www.bleepingcomputer.com/news/security/jadepuffer-ransomware-used-ai-agent-to-automate-entire-attack/){:target="_blank"}
