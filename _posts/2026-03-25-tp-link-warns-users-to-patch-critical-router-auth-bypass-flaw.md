---
title: 'TP-Link warns users to patch critical router auth bypass flaw'
date: 2026-03-25
permalink: /posts/2026/03/25/tp-link-warns-users-to-patch-critical-router-auth-bypass-flaw/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités critiques sur les routeurs TP-Link Archer NX

TP-Link a publié des correctifs de sécurité pour ses routeurs de la série Archer NX (modèles NX200, NX210, NX500 et NX600) afin de contrer plusieurs failles critiques. Ces vulnérabilités permettent, dans les cas les plus graves, une prise de contrôle totale de l'équipement par un attaquant non authentifié.

**Points clés :**
*   Les vulnérabilités permettent des actions privilégiées, allant de la modification de configuration à l'exécution de commandes arbitraires.
*   Le contexte est marqué par une pression accrue des autorités américaines (FCC, justice texane) concernant les risques de sécurité liés aux équipements réseau fabriqués à l'étranger.
*   Plusieurs vulnérabilités TP-Link sont déjà activement exploitées par des botnets comme Quad7.

**Vulnérabilités corrigées :**
*   **CVE-2025-15517 (Critique) :** Défaut d'authentification sur le serveur HTTP permettant à un attaquant non privilégié d'effectuer des opérations sensibles, notamment le téléchargement de nouveau firmware.
*   **CVE-2025-15605 :** Présence d'une clé cryptographique codée en dur permettant de déchiffrer, modifier et re-chiffrer les fichiers de configuration.
*   **CVE-2025-15518 et CVE-2025-15519 :** Failles d'injection de commandes permettant à un administrateur d'exécuter des commandes arbitraires sur le système.

**Recommandations :**
*   **Mise à jour immédiate :** Il est impératif de télécharger et d'installer la dernière version du firmware disponible sur le site officiel de TP-Link pour l'ensemble des modèles concernés.
*   **Responsabilité utilisateur :** Le constructeur souligne que le non-respect de ces mises à jour laisse les appareils exposés aux attaques et décline toute responsabilité quant aux conséquences d'une exploitation réussie.

---
[Source](https://www.bleepingcomputer.com/news/security/tp-link-warns-users-to-patch-critical-router-auth-bypass-flaw/){:target="_blank"}
