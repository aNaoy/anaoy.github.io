---
title: 'New TONTOU CPU attack bypasses Spectre v2 fixes, leaks Linux password hashes'
date: 2026-08-06
permalink: /posts/2026/08/06/new-tontou-cpu-attack-bypasses-spectre-v2-fixes-leaks-linux-password-hashes/
tags:
- veille-cyber
- bleepingcomp
---
### TONTOU : Une faille contourne les protections Spectre v2

Des chercheurs du MIT ont découvert **TONTOU** (Time-of-Neutralization to Time-of-Use), une technique d'attaque par canal auxiliaire qui contourne les mesures d'atténuation actuelles contre Spectre v2 (BTI - Branch Target Injection) sur les processeurs Intel et AMD.

**Points clés :**
* **Mécanisme :** L'attaque exploite le délai entre l'isolation du prédicteur de branchement et son utilisation réelle (le créneau TONTOU).
* **Injection d'interruptions :** Les chercheurs utilisent des interruptions logicielles pour forcer le noyau à exécuter un gestionnaire d'interruption. Ce dernier permet de "ré-empoisonner" les états microarchitecturaux du processeur avant qu'ils ne soient utilisés par la cible.
* **Impact :** La méthode permet l'extraction de données sensibles (comme les hashs de mots de passe du fichier `/etc/shadow`) à partir de la mémoire du noyau Linux.
* **Performances :** Sur un processeur AMD Zen 2, les chercheurs ont atteint une précision de 91,97 % pour l'extraction de données arbitraires.

**Vulnérabilités :**
* Bien que non associée à un identifiant CVE spécifique dans l'article, cette vulnérabilité découle d'une faille dans l'implémentation logicielle des protections existantes (`eIBRS` sur Intel et `Safe RET` sur AMD).
* L'attaque est facilitée par la possibilité pour un programme utilisateur non privilégié de manipuler le flux de contrôle du noyau via des interruptions.

**Recommandations :**
* AMD a publié un bulletin de sécurité (AMD-SB-7061) reconnaissant que le problème est lié à l'implémentation de `Safe RET` sous Linux.
* Les administrateurs systèmes doivent surveiller les correctifs futurs du noyau Linux et les mises à jour de microcode des fabricants (Intel/AMD) qui viseront à sécuriser la fenêtre critique entre le nettoyage et l'utilisation du prédicteur de branchement.
* Limiter, dans la mesure du possible, l'exécution de code arbitraire non audité sur les systèmes critiques.

---
[Source](https://www.bleepingcomputer.com/news/security/new-tontou-cpu-attack-bypasses-spectre-v2-fixes-leaks-linux-password-hashes/){:target="_blank"}
