---
title: 'Dell CSM Flaws Enable Unauthenticated Admin Access and Root on Kubernetes Nodes'
date: 2026-10-02
permalink: /posts/2026/10/02/dell-csm-flaws-enable-unauthenticated-admin-access-and-root-on-kubernetes-nodes/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans Dell Container Storage Modules (CSM)

Dell a publié des mises à jour correctives pour remédier à plusieurs failles critiques dans ses modules CSM, permettant potentiellement une prise de contrôle totale des systèmes de stockage et des clusters Kubernetes.

**Points clés :**
*   **Impact :** Les vulnérabilités permettent de contourner les contrôles d'authentification, d'obtenir des privilèges d'administrateur sur les baies de stockage et d'accéder au niveau root sur les nœuds Kubernetes.
*   **Portée :** L'ensemble des cinq familles de produits de stockage Dell supportées sont concernées.
*   **Version corrigée :** Toutes les versions antérieures à la 1.17.0 sont vulnérables. La mise à jour vers la version **1.18.0** est indispensable.

**Vulnérabilités identifiées :**
*   **CVE-2026-63688 (Score 10.0) :** Absence d'authentification dans le serveur gRPC (accès aux identifiants admin des baies).
*   **CVE-2026-63692 (Score 10.0) :** Défaut d'authentification dans le proxy d'autorisation (élévation de privilèges admin).
*   **CVE-2026-67269 (Score 9.9) :** Gestion inappropriée des privilèges (accès root sur les nœuds du cluster).
*   **CVE-2026-54472 (Score 9.8) :** Utilisation d'identifiants codés en dur (usurpation de jetons admin).
*   **CVE-2026-61421 (Score 9.8) :** Utilisation de clés cryptographiques codées en dur dans JWT.
*   **CVE-2026-67273 (Score 9.6) :** Injection dans le moteur de template (altération RBAC et lecture de secrets Kubernetes).

**Recommandations :**
1.  **Mise à jour immédiate :** Appliquer la version 1.18.0 du module CSM.
2.  **Rotation des secrets :** Renouveler impérativement tous les secrets de signature JWT après la mise à jour.
3.  **Absence de contournement :** Aucune mesure d'atténuation temporaire n'est disponible en dehors de l'installation du correctif officiel.

---
[Source](https://thehackernews.com/2026/10/dell-csm-flaws-enable-unauthenticated.html){:target="_blank"}
