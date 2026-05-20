---
title: 'GitHub Breached — Employee Device Hack Led to Exfiltration of 3,800+ Internal Repos'
date: 2026-05-20
permalink: /posts/2026/05/20/github-breached-employee-device-hack-led-to-exfiltration-of-3800-internal-repos/
tags:
- veille-cyber
- hackernews
---
### Compromission de GitHub : Exfiltration via une extension VS Code empoisonnée

GitHub a confirmé l'accès non autorisé à ses dépôts internes après que le groupe cybercriminel **TeamPCP** a mis en vente les données exfiltrées (environ 3 800 à 4 000 dépôts) sur un forum spécialisé. Cette brèche résulte de la compromission du poste de travail d'un employé via une extension malveillante de **Microsoft Visual Studio Code**.

#### Points clés
*   **Mode opératoire :** L'attaquant a utilisé une extension VS Code piégée pour compromettre l'appareil d'un employé, permettant le vol d'identifiants et l'accès aux dépôts internes de GitHub.
*   **Propagation :** TeamPCP mène une campagne de type "vers" baptisée **Mini Shai-Hulud**. Elle a récemment compromis le paquet PyPI `durabletask` de Microsoft, utilisé pour injecter un infostealer capable de récupérer des secrets cloud (AWS, Kubernetes, HashiCorp Vault), des clés SSH et des données de gestionnaires de mots de passe.
*   **Techniques avancées :** Le malware utilise des mécanismes comme « FIRESCALE » pour récupérer ses serveurs de commande et contrôle (C2) via des commits publics sur GitHub, assurant sa résilience.
*   **Collaboration :** Le groupe LAPSUS$ s'est associé à TeamPCP pour tenter de vendre les données exfiltrées pour 95 000 $.
*   **Impact :** Les dépôts concernés incluent des projets sensibles comme GitHub Actions, Copilot, CodeQL et l'infrastructure de gestion des Pull Requests.

#### Vulnérabilités et vecteurs
*   **Supply Chain Poisoning :** Empoisonnement de paquets open-source (ex: `durabletask` versions 1.4.1 à 1.4.3).
*   **Extension VS Code malveillante :** Vecteur d'accès initial sur le poste de travail.
*   **Vol de jetons (Token Theft) :** Utilisation de jetons d'authentification dérobés pour publier des paquets malveillants ou se propager dans des environnements cloud (AWS/K8s).

#### Recommandations
*   **Réinitialisation des accès :** GitHub a d'ores et déjà procédé à une rotation des secrets critiques ; les utilisateurs et entreprises doivent également auditer et renouveler leurs clés API et jetons d'accès si une compromission est suspectée.
*   **Audit des dépendances :** Vérifier l'intégrité des paquets utilisés dans les pipelines CI/CD. Toute machine ayant installé les versions infectées de `durabletask` doit être considérée comme compromise.
*   **Surveillance des extensions :** Restreindre l'installation d'extensions VS Code aux sources approuvées et surveiller les comportements anormaux des environnements de développement.
*   **Renforcement du contrôle d'accès :** Mettre en œuvre le principe du moindre privilège pour l'accès aux dépôts internes et aux services cloud, et limiter la durée de vie des jetons d'authentification.

---
[Source](https://thehackernews.com/2026/05/github-investigating-teampcp-claimed.html){:target="_blank"}
