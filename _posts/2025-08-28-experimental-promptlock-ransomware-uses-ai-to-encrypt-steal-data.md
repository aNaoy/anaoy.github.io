---
title: 'Experimental PromptLock ransomware uses AI to encrypt, steal data'
date: 2025-08-28
permalink: /posts/2025/08/28/experimental-promptlock-ransomware-uses-ai-to-encrypt-steal-data/
tags:
- veille-cyber
- bleepingcomp
---
**PromptLock : Le premier ransomware exploitant l'IA pour le vol et le chiffrement de données**

Une nouvelle menace logicielle, baptisée PromptLock, a été identifiée par des chercheurs en cybersécurité. Ce logiciel malveillant expérimental se distingue par son utilisation de l'intelligence artificielle, spécifiquement le modèle de langage gpt-oss:20b via l'API Ollama, pour générer dynamiquement des scripts Lua malveillants. Ces scripts sont conçus pour interagir avec les systèmes Windows, macOS et Linux, permettant l'énumération du système de fichiers, l'inspection des fichiers cibles, l'exfiltration de données et le chiffrement de ces dernières.

Le fonctionnement de PromptLock repose sur des instructions prédéfinies ("prompts") envoyées à un modèle linguistique hébergé sur un serveur distant, auquel le logiciel accède via un tunnel proxy. Il utilise ensuite l'algorithme de chiffrement SPECK 128-bit, un choix inhabituel pour un rançongiciel. Bien qu'une fonctionnalité de destruction de données ait été envisagée, elle n'a pas été implémentée dans la version découverte.

Les chercheurs estiment que PromptLock est actuellement une preuve de concept ou un projet en développement, plutôt qu'une menace active sur le terrain. Plusieurs indices soutiennent cette hypothèse, notamment l'utilisation d'un algorithme de chiffrement jugé faible, une adresse Bitcoin codée en dur apparemment liée à Satoshi Nakamoto, et l'absence de certaines fonctionnalités prévues. L'apparition de PromptLock souligne toutefois la capacité croissante à exploiter l'IA dans le développement de logiciels malveillants, offrant des avantages tels que la flexibilité opérationnelle, l'évasion des défenses et l'abaissement du seuil d'entrée dans la cybercriminalité. Cette évolution fait écho à la découverte récente du malware LameHug, qui utilise également un LLM pour générer des commandes de vol de données en temps réel.

**Points clés :**

*   **Technologie IA :** Utilisation de modèles linguistiques (gpt-oss:20b) pour générer des scripts malveillants dynamiquement.
*   **Langage de script :** Exploitation de Lua pour les actions malveillantes.
*   **Multiplateforme :** Ciblage des systèmes Windows, macOS et Linux.
*   **Fonctionnalités :** Énumération de fichiers, exfiltration de données, chiffrement.
*   **Algorithme de chiffrement :** SPECK 128-bit (considéré comme léger).
*   **Statut :** Découvert sur VirusTotal, considéré comme une preuve de concept ou un projet incomplet.
*   **Indicateurs de preuve de concept :** Chiffrement faible, adresse Bitcoin obsolète, fonctionnalité de destruction non implémentée.
*   **Implication générale :** Démontre la "weaponisation" de l'IA dans les flux de travail des malwares.

**Vulnérabilités / Capacités malveillantes :**

*   Vol de données sensibles via l'exfiltration.
*   Chiffrement de fichiers rendant les données inaccessibles sans la clé.
*   Énumération du système de fichiers pour identifier les cibles potentielles.
*   Potentiel de destruction de données (non implémenté dans la version découverte).

**Recommandations :**

Bien que cet article se concentre sur la découverte d'une nouvelle technique, les recommandations générales en matière de cybersécurité restent pertinentes pour atténuer les risques associés à ce type de menaces émergentes :

*   **Sensibilisation et formation :** Informer sur les nouvelles menaces basées sur l'IA.
*   **Surveillance et détection :** Mettre en place des systèmes de détection avancée capables d'identifier des comportements anormaux.
*   **Mises à jour et correctifs :** Maintenir les systèmes d'exploitation et les logiciels à jour pour corriger les vulnérabilités connues.
*   **Sauvegardes régulières :** Assurer des sauvegardes fiables et testées des données critiques.
*   **Sécurité des endpoints :** Utiliser des solutions de sécurité robustes sur les postes de travail et serveurs.
*   **Segmentation du réseau :** Limiter la propagation potentielle en cas d'infection.

---
[Source](https://www.bleepingcomputer.com/news/security/experimental-promptlock-ransomware-uses-ai-to-encrypt-steal-data/){:target="_blank"}
