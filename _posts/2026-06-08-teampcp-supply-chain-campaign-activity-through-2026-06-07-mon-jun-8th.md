---
title: 'TeamPCP Supply Chain Campaign: Activity Through 2026-06-07, (Mon, Jun 8th)'
date: 2026-06-08
permalink: /posts/2026/06/08/teampcp-supply-chain-campaign-activity-through-2026-06-07-mon-jun-8th/
tags:
- veille-cyber
- sans-isc
---
# Évolution et prolifération de la campagne "TeamPCP"

La campagne de compromission de la chaîne d'approvisionnement (supply chain) initiée par TeamPCP a franchi une étape critique : suite à la mise en libre accès du framework "Mini Shai-Hulud", les techniques d'attaque sont désormais reprises par des tiers, rendant l'attribution plus complexe. Le gouvernement américain, via la CISA, a formellement réagi, tandis que des vagues d'attaques automatisées (vers de réseau) ciblent les écosystèmes npm et CI/CD.

### Points clés
*   **Prolifération :** Le framework "Mini Shai-Hulud" a permis l'émergence de campagnes copycat, notamment "Miasma" (ciblant les paquets `@redhat-cloud-services`) et "Phantom Gyp" (ciblant `@vapi-ai/server-sdk`).
*   **Contournement des défenses :** Les attaquants exploitent des pipelines CI/CD compromis pour injecter du code malveillant dans des artefacts bénéficiant d'attestations de provenance SLSA valides.
*   **Évolution technique :** La variante "Phantom Gyp" utilise des fichiers `binding.gyp` pour exécuter du code lors de l'installation, échappant ainsi aux outils de détection basés uniquement sur les scripts `package.json`.
*   **Stagnation des extorsions :** Malgré l'intensité des attaques par "ver", les canaux d'extorsion liés à TeamPCP (Vect, CipherForce) demeurent inactifs.

### Vulnérabilités identifiées (CVE)
*   **CVE-2026-45321 :** Identifiant de suivi associé à TanStack/Mini Shai-Hulud.
*   **CVE-2026-48027 :** Code malveillant intégré dans le build v18.95.0 de Nx Console.
*   **CVE-2026-8398 :** Vulnérabilité liée à DAEMON Tools Lite.

### Recommandations pour les équipes de sécurité
*   **Remédiation immédiate :** Appliquer les correctifs liés aux CVE listées par la CISA avant le 10 juin 2026.
*   **Gestion des secrets :** Révoquer et renouveler systématiquement tous les jetons, secrets CI/CD et identifiants cloud accessibles depuis les pipelines de build.
*   **Audit et surveillance :** 
    *   Inspecter les journaux de CI/CD et les traces d'audit cloud.
    *   Élargir la détection des exécutions lors de l'installation au-delà du `package.json` en surveillant les hooks `binding.gyp` et `node-gyp`.
*   **Sécurisation du cycle de vie :** 
    *   Ne pas se fier uniquement aux attestations SLSA ; renforcer l'intégrité de l'environnement de build.
    *   Imposer l'authentification multifacteur (MFA) sur tous les comptes de maintenance de registres.
    *   Désactiver l'exécution automatique des scripts lors de l'installation dans les environnements CI, lorsque cela est possible.

---
[Source](https://isc.sans.edu/diary/rss/33060){:target="_blank"}
