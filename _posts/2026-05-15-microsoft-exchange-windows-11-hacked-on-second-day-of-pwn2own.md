---
title: 'Microsoft Exchange, Windows 11 hacked on second day of Pwn2Own'
date: 2026-05-15
permalink: /posts/2026/05/15/microsoft-exchange-windows-11-hacked-on-second-day-of-pwn2own/
tags:
- veille-cyber
- bleepingcomp
---
### Pwn2Own Berlin 2026 : Déferlante de failles Zero-Day sur les solutions d'entreprise

La conférence Pwn2Own Berlin 2026 a mis en lumière de multiples vulnérabilités critiques affectant des infrastructures d'entreprise majeures et des technologies d'intelligence artificielle. En seulement deux jours, 15 vulnérabilités de type "zero-day" ont été exploitées avec succès, permettant une exécution de code arbitraire sur des systèmes pourtant entièrement mis à jour.

**Points clés :**
*   **Domaines visés :** Serveurs (Exchange), systèmes d'exploitation (Windows 11, RHEL), outils de conteneurisation (NVIDIA Container Toolkit) et agents de codage basés sur l'IA (Cursor, OpenAI Codex).
*   **Impact financier :** Plus de 385 000 $ de primes ont été distribués aux chercheurs en sécurité le deuxième jour seulement.
*   **Processus de divulgation :** Conformément aux règles de la Zero Day Initiative (ZDI), les éditeurs concernés disposent d'un délai de 90 jours pour développer et déployer des correctifs.

**Vulnérabilités identifiées :**
*   **Microsoft Exchange :** Exécution de code à distance (RCE) avec privilèges SYSTEM via un enchaînement de trois failles logiques.
*   **Windows 11 :** Exploitation d'un dépassement d'entier (*integer overflow*) pour l'élévation de privilèges.
*   **NVIDIA Container Toolkit :** Exploitation via une faille de type *use-after-free*.
*   **Red Hat Enterprise Linux (RHEL) :** Élévation de privilèges vers le compte root.
*   **IA (Cursor/Codex) :** Plusieurs failles non spécifiées affectant les agents de codage.

*Note : Bien que les exploits soient confirmés, les identifiants CVE officiels ne sont pas encore attribués tant que les correctifs ne sont pas finalisés par les éditeurs.*

**Recommandations :**
*   **Surveillance proactive :** Étant donné le cycle de 90 jours imposé aux éditeurs, les administrateurs doivent surveiller étroitement les bulletins de sécurité de Microsoft, Red Hat et NVIDIA dans les prochains mois.
*   **Patch Management :** Prévoir une stratégie de déploiement rapide des mises à jour dès leur publication officielle.
*   **Sécurisation des outils IA :** Limiter l'accès aux agents de codage (comme Cursor) aux environnements isolés tant que les vulnérabilités ne sont pas corrigées.
*   **Défense en profondeur :** Ne pas se reposer uniquement sur les correctifs logiciels ; renforcer la segmentation réseau et la surveillance des comportements anormaux sur les serveurs critiques (Exchange) et les conteneurs.

---
[Source](https://www.bleepingcomputer.com/news/security/pwn2own-day-two-hackers-demo-microsoft-exchange-windows-11-red-had-enterprise-linux-zero-days/){:target="_blank"}
