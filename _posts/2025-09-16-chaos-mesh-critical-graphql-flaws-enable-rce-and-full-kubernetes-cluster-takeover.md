---
title: 'Chaos Mesh Critical GraphQL Flaws Enable RCE and Full Kubernetes Cluster Takeover'
date: 2025-09-16
permalink: /posts/2025/09/16/chaos-mesh-critical-graphql-flaws-enable-rce-and-full-kubernetes-cluster-takeover/
tags:
- veille-cyber
- hackernews
---
**Faille Critique dans Chaos Mesh : Détournement de Cluster Kubernetes**

Des chercheurs en cybersécurité ont découvert plusieurs vulnérabilités critiques dans Chaos Mesh, une plateforme d'ingénierie du chaos pour Kubernetes. Ces failles, exploitables avec un accès réseau minimal au sein du cluster, permettent à un attaquant de prendre le contrôle total du cluster, d'exécuter des injections de code arbitraires et de voler des jetons de compte de service.

**Points Clés :**

*   Les vulnérabilités résident dans le serveur GraphQL du Chaos Controller Manager, qui manquait de mécanismes d'authentification adéquats.
*   Un attaquant peut enchaîner ces vulnérabilités pour exécuter du code à distance sur l'ensemble du cluster.
*   Les actions malveillantes incluent l'arrêt de pods, l'interruption des communications réseau, l'exfiltration de données sensibles, la perturbation de services critiques et l'escalade de privilèges.

**Vulnérabilités Identifiées :**

*   **CVE-2025-59358** (CVSS 7.5) : Exposition d'un serveur GraphQL sans authentification permettant de tuer des processus arbitraires dans n'importe quel pod, menant à un déni de service à l'échelle du cluster.
*   **CVE-2025-59359** (CVSS 9.8) : Injection de commandes système d'exploitation dans la mutation `cleanTcs`.
*   **CVE-2025-59360** (CVSS 9.8) : Injection de commandes système d'exploitation dans la mutation `killProcesses`.
*   **CVE-2025-59361** (CVSS 9.8) : Injection de commandes système d'exploitation dans la mutation `cleanIptables`.

**Recommandations :**

*   Mettre à jour Chaos Mesh vers la version **2.7.3** ou supérieure dès que possible.
*   Si une mise à jour immédiate n'est pas possible, restreindre le trafic réseau vers le démon et le serveur API de Chaos Mesh.
*   Éviter d'exécuter Chaos Mesh dans des environnements ouverts ou mal sécurisés.

---
[Source](https://thehackernews.com/2025/09/chaos-mesh-critical-graphql-flaws.html){:target="_blank"}
