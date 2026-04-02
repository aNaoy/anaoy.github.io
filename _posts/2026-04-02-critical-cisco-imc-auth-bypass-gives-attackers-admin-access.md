---
title: 'Critical Cisco IMC auth bypass gives attackers Admin access'
date: 2026-04-02
permalink: /posts/2026/04/02/critical-cisco-imc-auth-bypass-gives-attackers-admin-access/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités critiques affectant les infrastructures Cisco

Cisco a récemment publié des correctifs pour plusieurs failles de sécurité majeures affectant ses serveurs et outils de gestion, exposant les systèmes à des prises de contrôle complètes.

**Points clés :**
*   **Contournement d'authentification IMC :** Une vulnérabilité critique permet à un attaquant non authentifié d'accéder aux serveurs Cisco (gammes UCS C-Series et E-Series) avec des privilèges d'administrateur.
*   **Exécution de code à distance (RCE) :** Une faille dans Cisco Smart Software Manager On-Prem permet l'exécution de commandes avec les privilèges root.
*   **Absence de contournement :** Pour la faille IMC, aucune mesure d'atténuation temporaire n'est disponible, rendant la mise à jour logicielle impérative.

**Vulnérabilités identifiées :**
*   **CVE-2026-20093 :** Contournement d'authentification dans Cisco IMC via une requête HTTP malveillante, permettant de modifier les mots de passe de n'importe quel utilisateur, y compris l'administrateur.
*   **CVE-2026-20160 :** RCE dans Cisco Smart Software Manager On-Prem, permettant à un utilisateur non privilégié d'exécuter des commandes sur le système d'exploitation sous-jacent avec des droits root.

**Recommandations :**
*   **Mise à jour immédiate :** Cisco recommande vivement d'appliquer les correctifs logiciels dès que possible pour l'ensemble des systèmes impactés.
*   **Vigilance accrue :** Bien qu'aucune exploitation active ne soit rapportée pour ces failles spécifiques, le contexte actuel (attaques par rançongiciels sur d'autres failles Cisco récemment corrigées) impose une réactivité maximale.

---
[Source](https://www.bleepingcomputer.com/news/security/critical-cisco-imc-auth-bypass-gives-attackers-admin-access/){:target="_blank"}
