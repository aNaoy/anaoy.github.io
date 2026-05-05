---
title: 'Cleartext Passwords in MS Edge&#x3f; In 2026&#x3f;, (Mon, May 4th)'
date: 2026-05-05
permalink: /posts/2026/05/05/cleartext-passwords-in-ms-edgex3f-in-2026x3f-mon-may-4th/
tags:
- veille-cyber
- sans-isc
---
### Vulnérabilité critique : Mots de passe en clair dans la mémoire de Microsoft Edge

Une faille de sécurité majeure affecte Microsoft Edge : les identifiants et mots de passe enregistrés par le navigateur sont stockés en texte clair dans la mémoire vive du processus. Il est possible d'extraire ces informations sensibles sans privilèges d'administrateur, simplement en créant un vidage mémoire (*dump*) du processus Edge et en utilisant l'outil `strings`.

**Points clés :**
* **Accessibilité :** N'importe quel utilisateur connecté (ou un logiciel malveillant exécuté sous son identité) peut extraire les mots de passe sans authentification supplémentaire.
* **Contraste de sécurité :** Bien que l'interface graphique de Edge exige une authentification (biométrie, code PIN) pour consulter les mots de passe, ces derniers restent librement accessibles dans la mémoire du système.
* **Réponse de Microsoft :** Le comportement est actuellement classé par Microsoft comme étant « intentionnel ».
* **Impact :** Cette vulnérabilité permet à un malware de récolter facilement l'ensemble des identifiants d'un utilisateur sans avoir à contourner le coffre-fort chiffré du navigateur.

**Vulnérabilités :**
* Aucune CVE n'a été attribuée à ce jour, Microsoft considérant ce comportement comme normal.

**Recommandations :**
* **Éviter le stockage natif :** Ne pas enregistrer les mots de passe directement dans Microsoft Edge.
* **Utiliser un gestionnaire de mots de passe dédié :** Privilégier des solutions tierces indépendantes qui chiffrent les bases de données de manière plus robuste et ne laissent pas les secrets en clair dans la mémoire volatile.
* **Prudence avec les logiciels tiers :** Étant donné la facilité d'extraction, limiter l'exécution de programmes non fiables sur la machine, car ceux-ci peuvent accéder aux données en mémoire en toute simplicité.

---
[Source](https://isc.sans.edu/diary/rss/32954){:target="_blank"}
