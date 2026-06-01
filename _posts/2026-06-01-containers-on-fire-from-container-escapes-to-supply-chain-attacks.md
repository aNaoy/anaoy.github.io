---
title: 'Containers on fire: from container escapes to supply chain attacks'
date: 2026-06-01
permalink: /posts/2026/06/01/containers-on-fire-from-container-escapes-to-supply-chain-attacks/
tags:
- veille-cyber
- securelist
---
### Sécurisation des infrastructures conteneurisées : menaces et vecteurs d'attaque

Les infrastructures modernes basées sur Docker et Kubernetes sont devenues des cibles privilégiées pour les cyberattaques. Celles-ci ne se limitent plus à la simple compromission d'un conteneur, mais visent désormais l'escalade de privilèges vers l'hôte, le vol de secrets Kubernetes et l'empoisonnement de la chaîne d'approvisionnement logicielle (supply chain).

#### Points clés
*   **Approche multi-étapes :** Les attaquants utilisent un conteneur comme point d'entrée pour infiltrer le système hôte ou le cluster Kubernetes.
*   **Le rôle des configurations :** Les erreurs de configuration (ex: privilèges excessifs, accès API non sécurisés) sont plus fréquemment exploitées que les vulnérabilités logicielles elles-mêmes.
*   **Chaîne d'approvisionnement :** L'empoisonnement d'images publiques ou la compromission des pipelines CI/CD permet d'injecter du code malveillant directement dans des environnements de confiance.
*   **Risque des APIs :** L'exposition non protégée des APIs (Docker, Kubernetes) offre aux attaquants un contrôle administratif total sur l'infrastructure.

#### Vulnérabilités notables
L'exploitation des failles du noyau Linux ou du moteur d'exécution (*runtime*) permet souvent de briser l'isolation :
*   **CVE-2019-5736 :** Permet d'écraser le binaire `runC` sur l'hôte, offrant un accès root à l'attaquant.
*   **CVE-2022-0492 :** Exploitation du mécanisme `cgroups release_agent` pour s'échapper du conteneur.
*   **CVE-2024-21626 :** Gestion défaillante des descripteurs de fichiers dans `runC`, facilitant l'accès au système de fichiers de l'hôte.

#### Recommandations de sécurité
*   **Principe du moindre privilège :** Bannir le mode `--privileged` et restreindre strictement les capacités Linux (ex: éviter `CAP_SYS_ADMIN`, `CAP_SYS_MODULE` ou `CAP_SYS_PTRACE`).
*   **Durcissement des APIs :** Sécuriser les APIs Docker/Kubernetes par authentification et chiffrement (TLS) ; ne jamais exposer ces services inutilement.
*   **Sécurisation de la supply chain :** Auditer systématiquement les images provenant de registres publics et protéger l'intégrité des pipelines CI/CD.
*   **Isolation et surveillance :** Utiliser des outils de protection du runtime pour surveiller les activités anormales à l'intérieur des conteneurs et limiter la portée des secrets (ServiceAccount tokens).
*   **Hygiène logicielle :** Maintenir les composants hôtes et les runtimes à jour pour corriger les vulnérabilités critiques du noyau.

---
[Source](https://securelist.com/container-attack-vectors/120010/){:target="_blank"}
