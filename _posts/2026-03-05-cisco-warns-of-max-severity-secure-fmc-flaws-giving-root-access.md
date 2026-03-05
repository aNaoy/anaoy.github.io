---
title: 'Cisco warns of max severity Secure FMC flaws giving root access'
date: 2026-03-05
permalink: /posts/2026/03/05/cisco-warns-of-max-severity-secure-fmc-flaws-giving-root-access/
tags:
- veille-cyber
- bleepingcomp
---
**Vulnérabilités Critiques dans Cisco Secure Firewall Management Center**

Cisco a publié des mises à jour pour corriger deux vulnérabilités d'une sévérité maximale dans son logiciel Secure Firewall Management Center (FMC). Ces failles permettent à des attaquants non authentifiés d'obtenir un accès système complet à distance.

**Points Clés :**

*   Le Secure FMC est une interface web ou SSH utilisée par les administrateurs pour gérer les pare-feux Cisco et configurer diverses fonctions de sécurité.
*   Les deux vulnérabilités peuvent être exploitées sans authentification préalable par des attaquants à distance.
*   Bien qu'il n'y ait pas de preuve actuelle d'exploitation active, Cisco a publié des correctifs pour prévenir d'éventuelles attaques.

**Vulnérabilités :**

*   **CVE-2026-20079 (Bypass d'authentification) :** Permet à un attaquant d'obtenir un accès "root" au système d'exploitation sous-jacent en envoyant des requêtes HTTP malveillantes.
*   **CVE-2026-20131 (Exécution de code à distance - RCE) :** Permet à un attaquant d'exécuter du code Java arbitraire en tant que "root" sur les appareils non corrigés en envoyant un objet Java sérialisé spécialement conçu via l'interface de gestion web.

Cette deuxième vulnérabilité affecte également le Cisco Security Cloud Control (SCC) Firewall Management.

**Recommandations :**

*   Appliquer immédiatement les mises à jour de sécurité publiées par Cisco pour le logiciel Secure Firewall Management Center (FMC).
*   Pour les versions affectées par CVE-2026-20131, il est également conseillé de vérifier la sécurité du Cisco Security Cloud Control (SCC) Firewall Management.

---
[Source](https://www.bleepingcomputer.com/news/security/cisco-warns-of-max-severity-secure-fmc-flaws-giving-root-access/){:target="_blank"}
