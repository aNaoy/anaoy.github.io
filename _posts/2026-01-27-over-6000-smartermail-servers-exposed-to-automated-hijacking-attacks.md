---
title: 'Over 6,000 SmarterMail servers exposed to automated hijacking attacks'
date: 2026-01-27
permalink: /posts/2026/01/27/over-6000-smartermail-servers-exposed-to-automated-hijacking-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Serveurs SmarterMail sous la menace d'un détournement critique

Plus de 6 000 serveurs SmarterMail sont exposés en ligne et potentiellement vulnérables à des attaques automatisées. Une faille d'authentification critique, identifiée comme CVE-2026-23760, permet à des attaquants non authentifiés de détourner des comptes administrateurs et d'exécuter du code à distance sur les serveurs compromis. La vulnérabilité réside dans le point d'accès de réinitialisation de mot de passe de l'API, qui ne vérifie pas la validité des requêtes et permet de réinitialiser les comptes d'administrateur sans vérification préalable.

**Points clés :**

*   **Vulnérabilité :** Contournement d'authentification critique dans l'API de réinitialisation de mot de passe de SmarterMail.
*   **Impact :** Permet aux attaquants non authentifiés de prendre le contrôle total des instances SmarterMail vulnérables en détournant les comptes administrateurs.
*   **Exploitation :** La faille est activement exploitée en masse via des attaques automatisées.
*   **Portée :** Plus de 6 000 serveurs SmarterMail ont été identifiés comme potentiellement vulnérables, avec des rapports indiquant plus de 8 550 instances encore exposées.
*   **Urgence :** La CISA a ajouté cette vulnérabilité à son catalogue des vulnérabilités exploitées et a ordonné aux agences gouvernementales américaines de sécuriser leurs serveurs sous trois semaines.

**Vulnérabilités :**

*   **CVE-2026-23760 :** Contournement d'authentification critique permettant la réinitialisation du mot de passe des comptes administrateur sans vérification.

**Recommandations :**

*   Les administrateurs de serveurs SmarterMail doivent impérativement appliquer le correctif fourni par SmarterTools, disponible dans la version build 9511.
*   Si les correctifs ne sont pas disponibles, il est recommandé d'arrêter l'utilisation du produit.
*   Pour les entités gouvernementales américaines, il est obligatoire de sécuriser les serveurs concernés avant le 16 février.

---
[Source](https://www.bleepingcomputer.com/news/security/over-6-000-smartermail-servers-exposed-to-automated-hijacking-attacks/){:target="_blank"}
