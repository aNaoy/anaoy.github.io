---
title: 'New Spectre-v2 BTR Attack Leaks Linux Memory Despite Existing Defenses'
date: 2026-09-29
permalink: /posts/2026/09/29/new-spectre-v2-btr-attack-leaks-linux-memory-despite-existing-defenses/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité BTR : Une nouvelle variante de Spectre-v2 ciblant les moteurs JIT

Une nouvelle variante de Spectre-v2, nommée **Branch Target Reuse (BTR)**, a été découverte par des chercheurs académiques. Cette faille exploite la manière dont les moteurs de compilation Just-In-Time (JIT) gèrent le code auto-modifiable et la prédiction de branchement indirect dans les processeurs modernes.

**Points clés :**
* **Mécanisme :** Contrairement aux protections actuelles, le CPU ne purge pas les anciennes entrées de prédiction de branchement (BTB) après la modification ou la libération de segments de code par le moteur JIT.
* **Exploitation :** Un attaquant peut forcer le processeur à utiliser une entrée de branchement obsolète ("stale entry"), provoquant une exécution spéculative vers une adresse contrôlée par l'attaquant.
* **Impact :** Cette vulnérabilité permet de contourner les protections logicielles existantes et d'accéder à des données sensibles (ex : hachage de mot de passe root) via des canaux auxiliaires.
* **Cibles identifiées :** Le noyau Linux (cBPF JIT), Mozilla Firefox (SpiderMonkey) et GraalVM.

**Vulnérabilités :**
* **CVE-2026-64507**
* **CVE-2026-64508**

**Recommandations :**
* **Noyau Linux :** Appliquer les correctifs de sécurité officiels intégrant les mitigations contre BTR.
* **GraalVM :** Utiliser la mise à jour qui implémente la randomisation des emplacements du cache de code JIT pour empêcher la réutilisation des régions mémoire.
* **Mozilla Firefox :** Poursuivre le déploiement de l'isolation des sites (Site Isolation) comme mesure de protection principale contre ce type d'exploitation.

---
[Source](https://thehackernews.com/2026/09/new-spectre-v2-btr-attack-leaks-linux.html){:target="_blank"}
