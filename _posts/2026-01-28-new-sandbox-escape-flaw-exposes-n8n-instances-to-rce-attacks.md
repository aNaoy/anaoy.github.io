---
title: 'New sandbox escape flaw exposes n8n instances to RCE attacks'
date: 2026-01-28
permalink: /posts/2026/01/28/new-sandbox-escape-flaw-exposes-n8n-instances-to-rce-attacks/
tags:
- veille-cyber
- bleepingcomp
---
**Faille critique dans n8n : Risque d'exécution de code à distance**

Deux vulnérabilités, identifiées sous les références CVE-2026-1470 et CVE-2026-0863, ont été découvertes dans la plateforme d'automatisation de flux de travail n8n. Ces failles, qui permettent l'évasion de bac à sable (sandbox escape), exposent les instances n8n auto-hébergées à des attaques d'exécution de code à distance (RCE), menaçant la confidentialité des données et le contrôle des systèmes sous-jacents.

**Points Clés :**

*   **Impact :** Les attaquants peuvent compromettre entièrement les instances n8n, accéder aux données sensibles et exécuter du code arbitraire sur l'hôte.
*   **Importance de n8n :** n8n est une plateforme d'automatisation open-source largement utilisée, avec plus de 200 000 téléchargements hebdomadaires, pour connecter des applications et des services, et qui supporte des intégrations avec l'IA et les grands modèles de langage (LLM).
*   **Difficulté du sandboxing :** Ces vulnérabilités soulignent la complexité de la sécurisation des langages dynamiques comme JavaScript et Python, où des comportements subtils du langage peuvent contourner les mesures de sécurité.
*   **Portée :** Seules les versions auto-hébergées de n8n sont affectées ; la plateforme cloud de n8n a déjà corrigé ces problèmes.

**Vulnérabilités :**

*   **CVE-2026-1470 :** Évasion de bac à sable JavaScript via une mauvaise gestion de l'instruction `with`. Permet l'exécution de JavaScript arbitraire et un RCE complet sur le nœud principal de n8n. Bien que nécessitant une authentification, sa criticité (9.9/10) réside dans la possibilité pour des utilisateurs non administrateurs de compromettre l'infrastructure.
*   **CVE-2026-0863 :** Évasion de bac à sable Python. Combine l'introspection d'objets basée sur les chaînes de format avec des comportements d'attribut d'erreur Python 3.10+ pour retrouver l'accès aux fonctions prédéfinies et aux importations restreintes. Permet l'exécution de commandes système et un RCE lorsque Python est exécuté en tant que sous-processus.

**Recommandations :**

*   **Mise à jour immédiate :** Les utilisateurs sont fortement encouragés à mettre à jour leurs instances n8n vers les versions corrigées dès que possible.
    *   CVE-2026-1470 : Corrigée dans les versions 1.123.17, 2.4.5 et 2.5.1.
    *   CVE-2026-0863 : Corrigée dans les versions 1.123.14, 2.3.5 et 2.4.2.

---
[Source](https://www.bleepingcomputer.com/news/security/new-sandbox-escape-flaw-exposes-n8n-instances-to-rce-attacks/){:target="_blank"}
