---
title: 'New Spectre v2 attack variant leaks Linux root password hash in minutes'
date: 2026-09-29
permalink: /posts/2026/09/29/new-spectre-v2-attack-variant-leaks-linux-root-password-hash-in-minutes/
tags:
- veille-cyber
- bleepingcomp
---
### BTR : Une nouvelle variante de Spectre v2 menace la sécurité Linux

La vulnérabilité **Branch Target Reuse (BTR)** constitue une nouvelle variante des attaques par exécution spéculative (Spectre v2). Elle permet à un attaquant d'exploiter les incohérences entre le prédicteur de branchement d'un processeur et le code réel en mémoire, notamment lorsqu'un moteur JIT (Just-In-Time) réutilise des adresses mémoire.

**Points clés :**
* **Fonctionnement :** L'attaque manipule les informations résiduelles du prédicteur de branchement pour forcer le processeur à exécuter temporairement des instructions erronées de manière spéculative, créant une fuite de données via le cache CPU.
* **Impact :** Les chercheurs ont démontré la capacité d'extraire le hash du mot de passe root d'un système Linux en seulement quelques minutes (entre 3 et 5 minutes selon le processeur).
* **Portée :** Bien que l'étude se soit concentrée sur le noyau Linux (cBPF) et des moteurs comme SpiderMonkey ou GraalVM, la vulnérabilité touche la majorité des processeurs modernes (Intel, AMD, Arm), car elle exploite une conception intrinsèque aux CPU actuels.

**Vulnérabilités :**
* **CVE-2026-64507**
* **CVE-2026-64508**

**Recommandations :**
* Appliquer immédiatement les mises à jour du système d'exploitation et du firmware fournies par les constructeurs.
* Mettre à jour le noyau Linux vers la version la plus récente, les correctifs ayant déjà été intégrés.

---
[Source](https://www.bleepingcomputer.com/news/security/new-spectre-v2-attack-variant-leaks-linux-root-password-hash-in-minutes/){:target="_blank"}
