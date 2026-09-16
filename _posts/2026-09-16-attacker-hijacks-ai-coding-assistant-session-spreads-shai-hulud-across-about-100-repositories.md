---
title: 'Attacker Hijacks AI Coding Assistant Session, Spreads Shai-Hulud Across About 100 Repositories'
date: 2026-09-16
permalink: /posts/2026/09/16/attacker-hijacks-ai-coding-assistant-session-spreads-shai-hulud-across-about-100-repositories/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne d'approvisionnement via un assistant de codage IA

Une intrusion ciblant un fournisseur SaaS a révélé une nouvelle méthode d'attaque exploitant l'IA générative. En piratant une session active d'un assistant de codage, un attaquant a incité un développeur à intégrer des dépendances logicielles empoisonnées, permettant l'injection du ver informatique « Shai-Hulud » dans une centaine de dépôts internes.

**Points clés :**
* **Vecteur d'attaque :** Utilisation d'une session d'assistant IA détournée pour suggérer des bibliothèques malveillantes.
* **Propagation :** Le ver Shai-Hulud s'est propagé latéralement dans l'infrastructure en exploitant des jetons OAuth GitHub volés.
* **Impact :** Exfiltration de secrets de développement et de code source, ainsi que la compromission du namespace officiel de l'entreprise.
* **Évolution des menaces :** Les attaquants utilisent désormais les LLM non plus seulement pour automatiser des tâches, mais comme vecteurs actifs de malware.

**Vulnérabilités :**
* Pas de CVE spécifique mentionnée, l'attaque repose sur l'exploitation d'une **session utilisateur active (Session Hijacking)** et sur l'**empoisonnement de dépendances (Supply Chain Attack)** dans les registres publics (PyPI/NPM).

**Recommandations :**
* **Validation rigoureuse :** Vérifier systématiquement les dépendances suggérées par l'IA via des sommes de contrôle cryptographiques et des listes blanches approuvées.
* **Isolation des secrets :** Stocker les clés d'API et les jetons OAuth hors de portée directe des extensions d'IA.
* **Contrôle des flux :** Centraliser et filtrer tout le trafic lié aux dépendances via des dépôts internes maîtrisés afin d'empêcher l'installation de paquets non vérifiés.

---
[Source](https://thehackernews.com/2026/09/attacker-hijacks-ai-coding-assistant.html){:target="_blank"}
