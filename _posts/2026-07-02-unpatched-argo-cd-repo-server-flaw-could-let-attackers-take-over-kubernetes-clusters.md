---
title: 'Unpatched Argo CD Repo-Server Flaw Could Let Attackers Take Over Kubernetes Clusters'
date: 2026-07-02
permalink: /posts/2026/07/02/unpatched-argo-cd-repo-server-flaw-could-let-attackers-take-over-kubernetes-clusters/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique non corrigée dans Argo CD : Risque de prise de contrôle de cluster

Une vulnérabilité critique affecte le composant `repo-server` d'Argo CD, permettant à un attaquant non authentifié d'exécuter du code arbitraire et de prendre potentiellement le contrôle total d'un cluster Kubernetes. Bien que signalée aux mainteneurs en janvier 2025, aucun correctif n'est disponible à ce jour.

**Points clés :**
*   **Vecteur d'attaque :** Le service gRPC interne `GenerateManifest` ne nécessite aucune authentification. Un attaquant peut détourner l'option `--helm-command` de l'outil `kustomize` pour exécuter un script malveillant.
*   **Escalade de privilèges :** Après avoir pris pied sur le `repo-server`, un attaquant peut récupérer les identifiants Redis (via des variables d'environnement), empoisonner le cache de déploiement et injecter des charges de travail malveillantes dans le cluster.
*   **Exposition :** L'attaque est facilitée par la configuration par défaut du chart Helm d'Argo CD, qui désactive les politiques réseau (`networkPolicy.create: false`), rendant le service accessible depuis n'importe quel pod compromis au sein du cluster.

**Vulnérabilités mentionnées :**
*   **Faille actuelle (repo-server) :** Aucune CVE attribuée (non corrigée).
*   **CVE-2024-31989 :** Vulnérabilité liée à l'absence de mot de passe Redis (précédemment exploitée).
*   **CVE-2025-55190 :** Fuite d'identifiants Git via des jetons d'accès en lecture seule.
*   **CVE-2026-42880 :** Exposition de secrets Kubernetes à des utilisateurs en lecture seule.

**Recommandations :**
*   **Isolation réseau :** Appliquer strictement des politiques réseau (`NetworkPolicies`) pour limiter l'accès aux ports du `repo-server` et de Redis aux seuls composants légitimes d'Argo CD.
*   **Audit de configuration :** Vérifier l'état actuel des politiques réseau via la commande `kubectl get networkpolicy -A`.
*   **Posture défensive :** Considérer le réseau interne du cluster comme un environnement hostile tant qu'un correctif officiel n'a pas été déployé par les mainteneurs.

---
[Source](https://thehackernews.com/2026/07/unpatched-argo-cd-repo-server-flaw.html){:target="_blank"}
