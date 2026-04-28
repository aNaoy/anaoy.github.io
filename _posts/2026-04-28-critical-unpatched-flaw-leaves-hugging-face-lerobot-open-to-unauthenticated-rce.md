---
title: 'Critical Unpatched Flaw Leaves Hugging Face LeRobot Open to Unauthenticated RCE'
date: 2026-04-28
permalink: /posts/2026/04/28/critical-unpatched-flaw-leaves-hugging-face-lerobot-open-to-unauthenticated-rce/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique d'exécution de code à distance dans LeRobot de Hugging Face

La plateforme de robotique open-source LeRobot de Hugging Face est affectée par une faille de sécurité critique permettant une exécution de code à distance (RCE) sans authentification. Cette vulnérabilité, qui touche les composants de serveur de politique et de client robot, découle de l'utilisation non sécurisée du format de sérialisation `pickle` pour traiter les données reçues via des canaux gRPC non chiffrés.

**Points clés :**
*   **Vecteur d'attaque :** L'attaquant envoie une charge utile `pickle` malveillante via les appels gRPC (`SendPolicyInstructions`, `SendObservations` ou `GetActions`).
*   **Impact :** Une compromission totale du système hôte, incluant le vol de données sensibles (clés API, identifiants SSH), le mouvement latéral au sein du réseau, ainsi que des risques de sécurité physique pour les robots connectés.
*   **Contexte :** Bien que Hugging Face ait développé le format *Safetensors* pour pallier les dangers de `pickle`, le framework LeRobot a continué d'utiliser `pickle.loads()` en ignorant délibérément les alertes de sécurité (`# nosec`).

**Vulnérabilité identifiée :**
*   **CVE-2026-25874** (Score CVSS : 9.3) : Désérialisation de données non fiables via `pickle`.

**Recommandations :**
*   **Mise à jour :** La vulnérabilité est confirmée sur la version 0.4.3 et reste présente dans les versions actuelles. Une correction est prévue pour la version 0.6.0. Il est conseillé aux utilisateurs de surveiller la sortie de cette mise à jour et d'appliquer le correctif dès sa disponibilité.
*   **Atténuation immédiate :** En attendant le correctif, restreindre strictement l'accès réseau au service `PolicyServer` pour empêcher toute communication non autorisée, car le service manque actuellement de mécanismes d'authentification et de chiffrement TLS.

---
[Source](https://thehackernews.com/2026/04/critical-cve-2026-25874-leaves-hugging.html){:target="_blank"}
