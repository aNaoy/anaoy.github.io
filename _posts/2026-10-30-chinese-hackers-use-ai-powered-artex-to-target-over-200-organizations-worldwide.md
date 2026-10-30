---
title: 'Chinese Hackers Use AI-Powered ARTEX to Target Over 200 Organizations Worldwide'
date: 2026-10-30
permalink: /posts/2026/10/30/chinese-hackers-use-ai-powered-artex-to-target-over-200-organizations-worldwide/
tags:
- veille-cyber
- hackernews
---
### Incursion à grande échelle par l'outil IA « ARTEX »

Le groupe cybercriminel chinois **Vapor Panda** (également connu sous le nom de *Earth Estries*) déploie massivement le framework d'automatisation **ARTEX**. Cet outil, reposant sur l'intelligence artificielle (DeepSeek et LLM commerciaux), permet à une équipe restreinte de mener des attaques simultanées contre plus de 200 organisations mondiales, incluant des ministères, des entreprises de défense et des fournisseurs de télécommunications.

#### Points clés
*   **Automatisation agentique :** ARTEX orchestre des agents autonomes pour coordonner la reconnaissance, l'exploitation et le mouvement latéral en parallèle, réduisant drastiquement le besoin d'intervention humaine manuelle.
*   **Multiplicité des vecteurs :** Les attaques ciblent simultanément les services cloud, les conteneurs, Active Directory, ainsi que les infrastructures VPN et de messagerie.
*   **Consommation de ressources :** L'intensité des attaques est telle qu'une seule intrusion peut consommer 1,4 milliard de jetons (tokens) LLM.
*   **Émergence de nouveaux groupes :** La menace s'étend avec l'identification de nouveaux acteurs (Hollow, Overcast, Titan et Veiled Panda) utilisant des outils propriétaires comme *FlowCloud* ou *IceGiant*.

#### Vulnérabilités et vecteurs d'attaque
*   **Injection XXE (XML External Entity) :** Chained avec des assertions SAML non signées pour interroger les services de métadonnées cloud.
*   **Désérialisation ViewState :** Exploitation d'une clé machine IIS codée en dur dans *Intapp Time Server* pour permettre l'exécution de code à distance (RCE).
*   **Abus de configuration :** Utilisation de clés d'authentification obsolètes, de mots de passe LAPS exposés et de la délégation contrainte basée sur les ressources pour usurper des comptes privilégiés.
*   **Techniques classiques :** Sideloading de DLL (pour le backdoor *FlowCloud*) et déploiement de web shells.

#### Recommandations
*   **Gestion des identités :** Appliquer une rotation stricte des clés d'authentification et supprimer tout certificat ou mot de passe hérité (depuis 2022 ou antérieur).
*   **Renforcement Cloud et Conteneurs :** Sécuriser les services d'orchestration de conteneurs (ne pas utiliser les configurations par défaut) et restreindre l'accès aux services de métadonnées cloud.
*   **Audit des accès :** Auditer les configurations Active Directory pour détecter l'usage abusif de la délégation contrainte et renforcer la protection des comptes administrateurs.
*   **Surveillance active :** Déployer des solutions de détection capables d'identifier des comportements anormaux au sein des accès VPN et des flux de messagerie, signes avant-coureurs d'une automatisation par IA.
*   **Gestion des vulnérabilités :** Mettre à jour immédiatement les logiciels tiers (type *Intapp Time*) et éviter l'utilisation de configurations par défaut pour les serveurs IIS.

---
[Source](https://thehackernews.com/2026/10/chinese-hackers-use-ai-powered-artex-to.html){:target="_blank"}
