---
title: 'Ruby Fixes Three Regex Engine Bugs Responsible for Four Critical GitLab RCE Flaws'
date: 2026-10-23
permalink: /posts/2026/10/23/ruby-fixes-three-regex-engine-bugs-responsible-for-four-critical-gitlab-rce-flaws/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans le moteur Regex de Ruby : Risque d'exécution de code à distance

Le langage Ruby a corrigé trois failles critiques au sein de son moteur d'expressions régulières (Onigmo), à l'origine de quatre vulnérabilités RCE (exécution de code à distance) exploitées initialement dans GitLab.

**Points clés :**
*   **Risque :** Les vulnérabilités permettent une corruption mémoire lors de la compilation d'une expression régulière.
*   **Périmètre :** Toute application utilisant Ruby qui génère des expressions régulières à partir de chaînes de caractères fournies par des utilisateurs (ex: `Regexp.new`, interpolation `/#{input}/`) est potentiellement vulnérable.
*   **Absence de solution alternative :** Les limites de temps (`Regexp.timeout`) ou de longueur de motif ne protègent pas contre ces failles.
*   **Fin de vie :** Ruby 3.2 et les versions antérieures ne recevront aucun correctif.

**Vulnérabilités identifiées (via GitLab) :**
*   **CVE-2026-97229** (Score 10.0) : Critique, exploitable sans authentification.
*   **CVE-2026-110264** (Score 10.0) : Critique, exploitable sans authentification, affectant GitLab depuis la version 7.0.
*   *Note :* Deux autres failles (non listées par CVE spécifique dans l'article, mais liées aux correctifs) nécessitaient initialement une authentification (Score 9.9).

**Recommandations :**
*   **Mise à jour immédiate :** Passer aux versions corrigées de Ruby :
    *   Ruby 4.0.9
    *   Ruby 3.4.12
    *   Ruby 3.3.13
*   **Administrateurs GitLab :** Mettre à jour vos instances vers les versions patchées (19.5.1, 19.4.3, 19.3.6, 19.2.9, 19.1.9, 19.0.10 ou 18.11.13).
*   **Développement :** Si la mise à jour est impossible, cesser immédiatement toute compilation d'expressions régulières basées sur des entrées utilisateur non fiables.
*   **Surveillance :** Utiliser les règles de détection publiées par GitLab pour identifier d'éventuelles tentatives d'exploitation.

---
[Source](https://thehackernews.com/2026/10/ruby-fixes-three-regex-engine-bugs.html){:target="_blank"}
