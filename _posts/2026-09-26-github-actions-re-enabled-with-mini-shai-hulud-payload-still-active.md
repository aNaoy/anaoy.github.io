---
title: 'GitHub Actions re-enabled with Mini Shai-Hulud payload still active'
date: 2026-09-26
permalink: /posts/2026/09/26/github-actions-re-enabled-with-mini-shai-hulud-payload-still-active/
tags:
- veille-cyber
- bleepingcomp
---
### Persistance de la menace Mini Shai-Hulud sur GitHub Actions

Deux dépôts GitHub Actions (`actions-cool/issues-helper` et `actions-cool/maintain-one-comment`), préalablement compromis lors de la campagne malveillante « Mini Shai-Hulud », ont été réactivés par leurs mainteneurs entre le 16 et le 25 septembre 2026 sans avoir été assainis. En conséquence, les pipelines CI/CD utilisant ces actions ont automatiquement téléchargé et exécuté du code malveillant dissimulé dans le fichier `index.js`.

**Points clés :**
* **Réactivation accidentelle :** La remise en ligne des dépôts avec des tags de version inchangés a réactivé la charge utile malveillante pour tous les workflows dépendants.
* **Impact étendu :** Environ 15 000 dépôts utilisent `issues-helper`. Le risque concerne particulièrement les workflows qui ne sont pas verrouillés sur un hash de commit spécifique.
* **Nature de la menace :** Le malware cible les jetons d'authentification, les identifiants et les secrets CI/CD des développeurs.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée à cet incident, car il s'agit d'une attaque par compromission de la chaîne d'approvisionnement (supply-chain attack) exploitant des dépôts tiers dont les tags de version pointent vers du code corrompu.

**Recommandations :**
* **Audit immédiat :** Identifier toutes les références aux actions `actions-cool/issues-helper` et `actions-cool/maintain-one-comment` dans vos projets.
* **Sécurisation des dépendances :** Remplacer les tags de version (mutables) par des hashs de commit vérifiés et propres.
* **Remédiation post-incident :** Si vos workflows ont été exécutés entre le 16 et le 25 septembre 2026, effectuez une rotation immédiate de tous les secrets, jetons et identifiants auxquels ces workflows avaient accès.
* **Examen des journaux :** Analyser les logs d'exécution des pipelines pour détecter toute activité suspecte survenue durant la période de réactivation.

---
[Source](https://www.bleepingcomputer.com/news/security/github-actions-re-enabled-with-mini-shai-hulud-payload-still-active/){:target="_blank"}
