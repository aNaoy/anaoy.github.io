---
title: 'Closing the Identity Gaps in Critical Infrastructure Security'
date: 2026-07-21
permalink: /posts/2026/07/21/closing-the-identity-gaps-in-critical-infrastructure-security/
tags:
- veille-cyber
- bleepingcomp
---
### Renforcer la sécurité des infrastructures critiques par l'identité et le Zero Trust

La protection des infrastructures critiques est devenue une priorité stratégique face à des acteurs étatiques persistants (ex: groupe Volt Typhoon) qui exploitent des vulnérabilités pour infiltrer les réseaux à long terme. La compromission des systèmes d'information (IT) est tout aussi critique que celle des systèmes opérationnels (OT), car les attaquants privilégient désormais la furtivité via des techniques de « vie sur le terrain » (living off the land).

**Points clés :**
* **Obsolescence de la confiance implicite :** Le modèle traditionnel basé sur la simple authentification est inefficace face au vol de credentials et aux détournements de sessions.
* **Complexité des environnements :** La difficulté de mettre à jour les systèmes OT legacy impose une approche de sécurité adaptative au niveau de l'accès des collaborateurs.
* **Stratégie de défense :** Le modèle Zero Trust doit évoluer au-delà de l'identité seule pour intégrer la vérification du contexte (utilisateur, appareil, état de conformité).

**Vulnérabilités exploitées :**
* **Comptes inactifs :** Comptes VPN sans authentification multi-facteurs (MFA).
* **Périphériques de périphérie (Edge) :** Failles dans les routeurs, pare-feux et appliances VPN.
* **Shadow IT :** Utilisation de dispositifs personnels (BYOD) non gérés par le service informatique.
* *Note : Bien que l'article mentionne des techniques d'attaques, aucune CVE spécifique n'est citée. Les vecteurs d'attaque classiques incluent le phishing, le vol de session et l'exploitation de vulnérabilités sur les équipements réseau.*

**Recommandations :**
* **Lier l'identité à l'appareil :** Garantir qu'un accès n'est accordé que si l'appareil est connu, sécurisé, chiffré et à jour.
* **Authentification résistante au phishing :** Imposer des méthodes d'authentification robuste qui empêchent l'accès depuis des terminaux non approuvés.
* **Visibilité et remédiation :** Maintenir un inventaire complet des terminaux accédant au réseau et automatiser la vérification de leur état de santé (posture) à chaque requête.
* **Segmentation et contrôle adaptatif :** Ajuster les accès en temps réel en fonction du contexte de l'utilisateur et de la criticité de la ressource visée.

---
[Source](https://www.bleepingcomputer.com/news/security/closing-the-identity-gaps-in-critical-infrastructure-security/){:target="_blank"}
